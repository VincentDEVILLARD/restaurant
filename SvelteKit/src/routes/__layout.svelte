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
			<a href="./contactUs"><p>Contact Us</p></a>
		</div>
		<div class="column" id="right">
			<a href="./privacy"><p>RGPD</p></a>
		</div>
	  </div> 

	<section class="copyrights">
		<div> © 2022 Refresh Brunch SARL</div>
	</section>
</footer>

<style>

	.copyrights {
		font-size: x-small;
		text-align: center;
		margin: 5px
	}

	footer {
		font-family:'Times New Roman', Times, serif;
	}

	.column {
		float: left;
		width: 50%;
	}

	.column > a > p {
		margin: 10px
	}

	#right {
		text-align: right;
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

</style>
