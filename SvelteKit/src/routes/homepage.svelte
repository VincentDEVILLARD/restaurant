<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>Notre Restaurant</title>
	<meta name="description" content="À propos de notre restaurant" />
</svelte:head>

<div class=Video>
	<video autoplay muted loop class="Video">
		<source src="/videohomepage.mp4" type="video/mp4">
	</video>
	<div class="caption">
		<h3>Un super super nom de restaurant</h3>
		<h4>Avec un sous titre pour expliquer en quelques mots ce qu'on sert dans le restaurant. Il peut s'étendre sur plusieurs lignes.</h4>
	</div>
</div>

<div class="main">	

		<main class="Carousel">

			<div class="container">
			 
			  <div class="slideshow">
				<div class="box">
				  <!-- svelte-ignore a11y-missing-attribute -->
				  <img src="/img/kousbi1.jpg">
				  <span>La Salle</span>>
				</div>
				<div class="box">
				  <!-- svelte-ignore a11y-missing-attribute -->
				  <img src="/img/kousbi2.png">
				  <span>L'Équipe</span>
				</div>
				<div class="box">
				  <!-- svelte-ignore a11y-missing-attribute -->
				  <img src="/img/kousbi3.png">
				  <span>La Nourriture</span>
				</div>
	
			  </div>
	
			</div>
	
		</main>
	
</div>

<style>
	.Video {
		height: 100vh;
		width: 100%;
		position: relative;
	}

	.Video video {
		width: 100%;
		height: 100%;
		position: absolute;
		object-fit: cover;
		z-index: 0;
	}

	.Video .caption {
		z-index: 1;
		position: relative;
		text-align: left;
		color: #ffffff;
		padding: 10px;
	}

	h3 {
		color:#ffffff;
		font-size: 10vh;
		font-family: 'Times New Roman', Times, serif;
		text-shadow: 2px 2px black;
	}

	h4 {
		color:#ffffff;
		font-size: 3vh;
		font-family: 'Times New Roman', Times, serif;
		text-shadow: 1px 1px black;
	}
</style>