<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main>
	<slot />
</main>

<footer>      
		<div class="nav">
		  <a class="nav-link" href="PAS DE LIEN ENCORE">À propos</a>
		  <a class="nav-link" href="PAS DE LIEN ENCORE">Livraisons</a>
		  <a class="nav-link" href="PAS DE LIEN ENCORE">RGPD</a>
		  <a class="nav-link" href="PAS DE LIEN ENCORE">Contact</a>
		</div>
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100%;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
