
<main>
	<body>
        <h2>supabase</h2>

	<div>
        <script>
		import { supabase } from "/src/supabaseClient.ts";


		const { data, error } = await supabase
			.from('Recrutements')
			.select('*')


        </script>
	</div>
    </body>
</main>


<style>
	
</style>