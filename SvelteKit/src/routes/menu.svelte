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
    <style type="text/css">
        @import url(app.css);;
    </style>
</svelte:head>

<div class="main-menu">
    <div class="menu-header">
        <h1 class="menu-header_title">Cartes & Menus</h1>
    </div>

    <div class="menu-category">
		<a href="#brunch"><div class="colonne1"><h2>Brunch</h2><p>(10h-15h)</p></div></a>
		<a href="#tapas"><div class="colonne2"><h2>Tapas</h2><p>(18h-00h)</p></div></a>
		<a href="#boissons"><div class="colone3"><h2>Carte des<br/>boissons</h2></div></a>
        <div class="hline"></div>
    </div>

<div class="menu-list">
    <!--Ajouter scroll navigation pour pas de défilement-->
    <br/><br/>
	<h2 class="menu-list_title" id="brunch">Brunch (10h-15h)</h2>
        <!-- ajouter photo-->
    <div class="vline"></div>
		<h3 class="menu-list_subcategory">Salé</h3>	
		<div>
		    <!-- Liste menu brunch salé - petites faims -->
			<h4 class="menu-list_subcategory2">Salé - petites faims</h4>
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
                <p>Description 1</p><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
                <p>Description 2</p><br/>
			</div>
            <div class="vline"></div>
				<!--Liste menu brunch salé - grandes faims-->
				<h4 class="menu-list_subcategory2">Salé - grandes faims</h4>
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
                <p>Description 1</p><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
                <p>Description 2</p><br/>
			</div>
		</div>
        <div class="vline"></div>
		<h3 class="menu-list_subcategory">Sucré</h3>
		<div>
			<!--Liste menu brunch sucré-->
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
                <p>Description 1</p><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
                <p>Description 2</p><br/><br/>
			</div>
		</div>

	<h2 class="menu-list_title" id="tapas">Tapas (18h-00h)</h2>
    <!-- ajouter photo-->
    <div class="vline"></div>
		<!--Liste menu tapas - plateaux découvertes-->
		<div>
			<h3 class="menu-list_subcategory">Plateaux Découvertes (2 personnes)</h3>	
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
                <p>Description 1</p><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
                <p>Description 2</p><br/>
			</div>
		</div>
		<!--Liste menu tapas - petites portions-->
		<div>
            <div class="vline"></div>
			<h3 class="menu-list_subcategory">Petites Portions</h3>	
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
                <p>Description 1</p><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
                <p>Description 2</p><br/>
			</div>
		</div>
		<!--Liste menu tapas - desserts-->
		<div>
            <div class="vline"></div>

			<h3 class="menu-list_subcategory">Desserts</h3>	
            <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
            <p>Description 1</p><br/>
            <br/>
            <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
            <p>Description 2</p><br/><br/>
		</div>
        
	<h2 class="menu-list_title" id="boissons">Carte des boissons</h2>
        <!-- ajouter photo-->
        <div class="vline"></div>
		<!--Liste menu carte des boissons - sans alcool -->
		<div>
			<h3 class="menu-list_subcategory">Sans Alcool</h3>	
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/><br/>

                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/><br/>
			</div>
		</div>
		<!--Liste menu alcool-->
		<div>
            <div class="vline"></div>
			<h3 class="menu-list_subcategory">Alcool</h3>	
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/><br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/><br/>
			</div>
		</div>
		<!--Liste menu boissons chaudes-->
		<div>
            <div class="vline"></div>
			<h3 class="menu-list_subcategory">Boissons Chaudes</h3>	
            <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/><br/>
            <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/><br/>
		</div>
	</div>

</div>
<div>
    <p style="text-align: center;font-size: 1.2em;font-weight:bold;letter-spacing:0.5px">Bon appétit !</p>
</div>
<footer>

</footer>

<style>
.menu-header {
	margin: 10px;
	padding: 20px;
	background-image: url("file:///Users/margotclavel/Downloads/davey-gravy-krsKfCC1lYw-unsplash.jpg");
}
.menu-header_title {
	font-family: 'Playfair Display', serif;
	margin: 10px;
    text-align: center;
	font-weight: bold;
	text-transform: uppercase;
}

.menu-category {
	color: var(--color_primary);
	margin: 20px 0;
	text-align: center;
	text-transform: uppercase;
}
.menu-category h2 {
	font-family: 'Playfair Display', serif;
	font-size: 1.5rem;
	line-height: 1.375;
	letter-spacing: 2px;
	color: #111;
	margin: 0;
	text-align: center;
}

.colonne1, .colonne2, .colonne3 {
    width:30%;
    float:left;
    /* ajouter hover souris */
}
.hline { 
    display: block;
    height: 1px;
    border: 0;
    border-top: 1px solid #ccc;
    margin: 1em 0;
    margin-left:20% !important; 
    margin-right:20% !important;
    width: 60%;
}
.vline { 
    display: block;
    height: 0px;
    border: 0;
    border-top: 40px solid #ccc;
    margin: 0.5em 0;
    margin-left:50% !important; 
    margin-right:50% !important;
    width: 1px;
}
.menu-category p {
	font-family: 'Playfair Display', serif;
	letter-spacing: 2px;
	color: #111;
	margin: 0;
	text-align: center;
}
.menu-list {
	/* Ajouter scroll navigation pour pas de défilement */
	font-weight: bold;
}
.menu-list_title {
	font-family: 'Playfair Display', serif;
	font-size: 1.5rem;
	line-height: 1.375;
	letter-spacing: 2px;
	color: #111;
	margin: 0;
	letter-spacing: 2px;
	text-align: center;
	font-weight: bold;
	text-transform: uppercase;
}
.menu-list_subcategory {
   	text-align: center;
	color: grey;
    line-height: 0;
}
.menu-list_subcategory2 {
   	text-align: center;
}
.menu-list p {
	font-family: 'Playfair Display', serif;
	font-weight: normal;
	line-height: 0;
	text-align: left;
}

.menu-list p {
	text-align: justify;
}
.menu-list p span.gauche {
	float: left;
}
.menu-list p span.droite {
	float: right;
}
</style>
