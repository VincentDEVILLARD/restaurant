<script>
// @ts-nocheck
	import '../app.css';
	import "carbon-components-svelte/css/g10.css";
	import { supabase } from "/src/supabaseClient.ts";
    import * as yup from "yup";
    import { createForm } from "svelte-forms-lib";
	import { page } from '$app/stores';

    import { TextInput, TextArea, Button, FormGroup, Form, Checkbox, InlineNotification, DatePicker, DatePickerInput } from "carbon-components-svelte";

	const validationSchema = yup.object().shape({
      name: yup.string().required('Please enter a name'),
      email: yup.string().email().required('Please enter a valid email'),
      message: yup.string().required('Please enter a message')
	});

    let apiResult = null;

    const { form, errors, handleChange, handleSubmit, isSubmitting, handleReset } = createForm({
        initialValues: { name: "", email: "", message: "" },
        validationSchema: validationSchema,
        onSubmit: async values => {

            try {
                var result = await supabase.from("Recrutements").insert(values);

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

				<h2>Do you want to join us?</h2>
				<p>Enter your information on this form and we will contact you soon !</p> <br/><br/>
			
				{#if apiResult != null}
			
					{#if apiResult == true}
					<InlineNotification
						lowContrast
						kind="success"
						title="Success:"
						subtitle="Your candidacy has been received."
					/>
					{:else}
					<InlineNotification lowContrast kind="error"
						title="Error:"
						subtitle="A server error occurred. No job for you."
					/>
			
					{/if}    
				{/if}

				<Form on:submit={handleSubmit}>

					<FormGroup>
						<TextInput labelText="Name" name="name" 
							on:change={handleChange} bind:value={$form.name}
							invalid={$errors.name.length > 0} invalidText={$errors.name}/>
					</FormGroup>

					<FormGroup>
						<TextInput labelText="First Name" name="prenom" 
							on:change={handleChange} bind:value={$form.prenom}
							invalid={$errors.name.length > 0} invalidText={$errors.name}/>
					</FormGroup>

					<FormGroup>
						<TextInput labelText="Phone Number" name="Telephone" 
							on:change={handleChange} bind:value={$form.telephone}
							invalid={$errors.name.length > 0} invalidText={$errors.name}/>
					</FormGroup>

					<FormGroup>
						<TextInput labelText="Email" name="email" type="email" 
							on:change={handleChange} bind:value={$form.email}
							invalid={$errors.email.length > 0} invalidText={$errors.email}/>
					</FormGroup>

					<FormGroup>
						<DatePicker datePickerType="single" on:change={handleChange} bind:value={$form.disponibilite}>
							<DatePickerInput labelText="Starting Date" placeholder="dd/mm/yyyy" />
						</DatePicker>
					</FormGroup>

					<p>When are you available?</p> <br/><br/>

					<FormGroup>
						<Checkbox id="semaine" labelText="Weekdays (Mondays to Fridays)" 
							on:change={handleChange} bind:value={$form.semaine}/>
					</FormGroup>

					<FormGroup>
						<Checkbox id="weekend" labelText="Weekends (Saturdays & Sundays)" 
							on:change={handleChange} bind:value={$form.weekend}/>
					</FormGroup>
			
					<FormGroup>
						<TextArea labelText="Motivation letter" name="message" type="textarea"
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


			<br>

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
		text-align: left;
		width: 100em;
	}

	#admin {
		text-align: center;
		background-color:rgb(255, 255, 255);
		color:rgb(255, 255, 255)
	}
</style>