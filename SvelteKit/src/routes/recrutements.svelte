<script>
// @ts-nocheck


	import '../app.css';
	import "carbon-components-svelte/css/g10.css";
	import { supabase } from "/src/supabaseClient.ts";
    import * as yup from "yup";
    import { createForm } from "svelte-forms-lib";

    import { TextInput, TextArea, Button, FormGroup, Form, InlineNotification } from "carbon-components-svelte";

    let apiResult = null;

	const validationSchema = yup.object().shape({
      name: yup.string().required('Please enter a name'),
      email: yup.string().email().required('Please enter a valid email'),
      message: yup.string().required('Please enter a message')
	});

    const { form, errors, handleChange, handleSubmit, isSubmitting, handleReset } = createForm({
        initialValues: { Prénom: "", Téléphone: "", Email: "" },
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

		<h2>Contact Us</h2>
		<p>Enter the details to get in touch with us. You can remove your email at any time after this.</p> <br/><br/>
	
		{#if apiResult != null}
	
			{#if apiResult == true}
			<InlineNotification
				lowContrast
				kind="success"
				title="Success:"
				subtitle="Your message has been received"
			/>
			{:else}
			<InlineNotification lowContrast kind="error"
				title="Error:"
				subtitle="An internal server error occurred."
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
				<TextInput labelText="Email" name="email" type="email" 
				on:change={handleChange} bind:value={$form.email}
				invalid={$errors.email.length > 0} invalidText={$errors.email}/>
			</FormGroup>
	
	
			<FormGroup>
				<TextArea labelText="Message" name="message" type="textarea"
				on:change={handleChange} bind:value={$form.message}
				invalid={$errors.message.length > 0} invalidText={$errors.message}/>
			</FormGroup>
	
			<Button type="submit" disabled={$isSubmitting}>Submit</Button>
		</Form>
	</div>
</main>


<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100%;
		margin: 0 auto;
		box-sizing: border-box;
	}

	@media (min-width: 480px) {
	}

	.page {
        margin: 40px;
    }
</style>