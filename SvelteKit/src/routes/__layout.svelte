<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main>
	<slot />
</main>

<footer>      
	<div class="row">
		<div class="column" id="left">
			<p>Contact Us</p>
		</div>
		<div class="column" id="right">
			<p>RGPD</p>
		</div>
	  </div> 
</footer>

<style>

	#left > p {
		justify-content:left
	}

	.column {
		float: left;
		width: 50%;
	}

	.row:after {
		content: "";
		display: table;
		clear: both;
	}

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
