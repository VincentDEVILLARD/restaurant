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

<div class="main-menu">
	<div class="menu-header" style="background-image:url(https://www.auteuil-brasserie.com/i/auteuil-brasserie/3/4/1/1/8/1/1/5/0/9/9/3/6/1601022541_185/5c3f765351ab6417829beac6be8a47d9.website_hd.jpg)">
			<div class="row page-header__content narrow">
				<article class="col-full">
					<h1 class="menu-header_title">Cartes & Menus</h1>
				</article>
			</div>
	</div>

	<div class="menu-category">
	<h2> Brunch </h2><p> (10h-15h) </p>
	<h2> Tapas </h2><p> (18h-00h) </p>
	<h2> Carte des boissons </h2>
	</div>
</div>