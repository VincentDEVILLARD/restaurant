
<script>
// @ts-nocheck
	

	import { supabase } from "/src/supabaseClient.ts";

	async function getData() {
		const { data, error } = await supabase
			.from('Recrutements')
			.select()  
			
		if (error) throw new Error(error.message)
		
		return data
	}
</script>

<main>
	<body>
	<div>

		<h1>Applications</h1>
		
		{#await getData()}
			<p>Fetching data...</p>
			{:then data}
			{#each data as cand}
				<h2>Candidacy n°{cand.id}</h2>
				<p>Information on the candidate</p>
				<li>{cand.name}</li>
				<li>{cand.prenom}</li>
				<li>{cand.telephone}</li>
				<li>{cand.email}</li>
				<br>
				<p>Possible starting date</p>
				<li>{cand.disponibilite}</li>
				<p>Available during the week?</p>
				<li>{cand.semaine}</li>
				<p>Available on weekends?</p>
				<li>{cand.weekend}</li>
				<br>
				<p>Motivation letter</p>
				<li>{cand.motivation}</li>
				<br>
				<hr>
			{/each}
			{:catch error}
			<p>Something went wrong while fetching the data:</p>
			<pre>{error}</pre>
		{/await}


	</div>
    </body>
</main>


<style>
		main {
        margin: 40px;
	}

	h2 {
		font-size:x-large;
	}
</style>