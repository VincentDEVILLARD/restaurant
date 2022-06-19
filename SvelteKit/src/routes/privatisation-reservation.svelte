<script>
// @ts-nocheck
import '../app.css';
	import "carbon-components-svelte/css/g10.css";
	import { supabase } from "/src/supabaseClient.ts";
    import * as yup from "yup";
    import { createForm } from "svelte-forms-lib";
	import { page } from '$app/stores';

    import { TextArea, Button, FormGroup, Form, InlineNotification, DatePicker, DatePickerInput, TimePicker, TimePickerSelect, SelectItem, NumberInput } from "carbon-components-svelte";

	const validationSchema = yup.object().shape({
      message: yup.string().required('Please enter a message')
	});

    let apiResult = null;

    const { form, errors, handleChange, handleSubmit, isSubmitting, handleReset } = createForm({
        initialValues: { name: "", email: "", message: "" },
        validationSchema: validationSchema,
        onSubmit: async values => {

            try {
                var result = await supabase.from("Reservation").insert(values);

                if (result.data != null) {
                    apiResult = true;
                } else {
                    apiResult = false;
                }

            } catch (ex) {
                apiResult = false;
            }

            handleReset();
      }
    });
</script>

<main>

			<div class="page">

				<h2>Book a table</h2>
                <br>
			
				{#if apiResult != null}
			
					{#if apiResult == true}
					<InlineNotification
						lowContrast
						kind="success"
						title="Success:"
						subtitle="Your reservation has been received."
					/>
					{:else}
					<InlineNotification lowContrast kind="error"
						title="Error:"
						subtitle="Oops. Server error. No food for you."
					/>
			
					{/if}    
				{/if}

				<Form on:submit={handleSubmit}>

                    <FormGroup>
                        <NumberInput on:change={handleChange} bind:value={$form.number}
                            max={50}
                            invalidText="Number of guest for a reservation must be at least 4 and maximum 50."
                            helperText="Our restaurant can accomodate a maximum of 50 guests."
                            label="How many guests?"
                            />
                    </FormGroup>

                    <div class="row">
                        <div class="column">					
                            <FormGroup>
                                <DatePicker datePickerType="single" on:change={handleChange} bind:value={$form.date}>
                                    <DatePickerInput labelText="Pick a date" placeholder="dd/mm/yyyy" />
                                </DatePicker>
                            </FormGroup></div>

                        <div class="column">
                            <FormGroup>
                                <TimePicker on:change={handleChange} bind:value={$form.time} labelText="And a time" placeholder="hh:mm">
                                    <TimePickerSelect value="pm">
                                      <SelectItem value="am" text="AM" />
                                      <SelectItem value="pm" text="PM" />
                                    </TimePickerSelect>
                                </TimePicker>
                            </FormGroup>
                        </div>
                    </div> 
			
					<FormGroup>
						<TextArea labelText="Anything to add? (Birthday, Allergies, Commentary...)" name="message" type="textarea"
							on:change={handleChange} bind:value={$form.message}
							invalid={$errors.message.length > 0} invalidText={$errors.message}/>
					</FormGroup>

					<div id="submit">
					<Button type="submit" disabled={$isSubmitting}>Submit</Button>
					</div>
				</Form>
			</div>

			<br>

			<p id=admin class:active={$page.url.pathname === '/database'}>
				<a sveltekit:prefetch href="/database" id=admin>Database</a>
			</p>
</main>



<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100%;
		margin: 0 auto;
		box-sizing: border-box;
		background-color:rgb(255, 255, 255);
	}

	@media (max-width: 1000px) {

	}

	.page {
        margin: 40px;
        font-family: 'Times New Roman', Times, serif;
    }

	#submit {
		text-align: center;
		width: 100%;
	}

	#admin {
		text-align: center;
		background-color:rgb(255, 255, 255);
		color:rgb(255, 255, 255)
	}

    .column {
        float: left;
        margin: 5px
    }


    .row:after {
        content: "";
        display: table;
        clear: both;
    }
</style>
    