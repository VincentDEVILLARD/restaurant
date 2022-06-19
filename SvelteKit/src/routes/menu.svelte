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
    <title>Refresh Brunch</title>
    <meta name="description" content="Refresh Brunch Menu" />
    <style type="text/css">
        @import url(app.css);;
    </style>
</svelte:head>

<div class="main-menu">
    <div class="menu-header">
        <br/><h1 class="menu-header_title">Menu</h1><br/>
    </div>

    <div class="menu-category"><br/>
			<a href="#brunch"><div class="colonne1"><h2>Brunch</h2><p>(10h-15h)</p></div></a>
			<a href="#tapas"><div class="colonne2"><h2>Tapas</h2><p>(18h-00h)</p></div></a>
			<a href="#drinks"><div class="colone3"><h2>Drinks</h2></div></a><br/><br/>
        	<div class="hline"></div>
    </div>

<div class="menu-list">
    <!--Ajouter scroll navigation pour pas de défilement-->
    <br/><br/>
	<h2 class="menu-list_title" id="brunch">Brunch (10h-15h)</h2>
        <!-- ajouter photo-->
    <div class="vline"></div>
		<h3 class="menu-list_subcategory">Salted</h3>	
		<div>
		    <!-- Liste menu brunch salé - petites faims -->
			<h4 class="menu-list_subcategory2">Salted - Little Hunger</h4>
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
                <p class="description">Description 1</p><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
                <p class="description">Description 2</p><br/>
			</div>
            <div class="vline"></div>
				<!--Liste menu brunch salé - grandes faims-->
				<h4 class="menu-list_subcategory2">Salted - Big Hunger</h4>
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
                <p class="description">Description 1</p><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
                <p class="description">Description 2</p><br/>
			</div>
		</div>
        <div class="vline"></div>
		<h3 class="menu-list_subcategory">Sweet</h3>
		<div>
			<!--Liste menu brunch sucré-->
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
                <p class="description">Description 1</p><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
                <p class="description">Description 2</p><br/><br/>
			</div>
		</div>

	<h2 class="menu-list_title" id="tapas">Tapas (18h-00h)</h2>
    <!-- ajouter photo-->
    <div class="vline"></div>
		<!--Liste menu tapas - plateaux découvertes-->
		<div>
			<h3 class="menu-list_subcategory">Discovery (2 persons)</h3>	
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
                <p class="description">Description 1</p><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
                <p class="description">Description 2</p><br/>
			</div>
		</div>
		<!--Liste menu tapas - petites portions-->
		<div>
            <div class="vline"></div>
			<h3 class="menu-list_subcategory">Small Bites</h3>	
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
                <p class="description">Description 1</p><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
                <p class="description">Description 2</p><br/>
			</div>
		</div>
		<!--Liste menu tapas - desserts-->
		<div>
            <div class="vline"></div>

			<h3 class="menu-list_subcategory">Desserts</h3>	
            <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/>
            <p class="description">Description 1</p><br/>
            <br/>
            <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/>
            <p class="description">Description 2</p><br/><br/>
		</div>
        
	<h2 class="menu-list_title" id="drinks">Drinks</h2>
        <!-- ajouter photo-->
        <div class="vline"></div>
		<!--Liste menu carte des boissons - sans alcool -->
		<div>
			<h3 class="menu-list_subcategory">Soft Drinks</h3>	
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/><br/>

                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/><br/>
			</div>
		</div>
		<!--Liste menu alcool-->
		<div>
            <div class="vline"></div>
			<h3 class="menu-list_subcategory">Hard Drinks</h3>	
			<div>
                <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/><br/>
                <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/><br/>
			</div>
		</div>
		<!--Liste menu boissons chaudes-->
		<div>
            <div class="vline"></div>
			<h3 class="menu-list_subcategory">Hot Drinks</h3>	
            <p><span class="gauche" style="font-weight: bold">Titre 1</span><span class="droite" style="font-style:italic;color:grey">Prix 1</span></p><br/><br/>
            <p><span class="gauche" style="font-weight: bold">Titre 2</span><span class="droite" style="font-style:italic;color:grey">Prix 2</span></p><br/><br/>
		</div>
	</div>

</div>
<div>
    <p style="text-align: center;font-size: 1.2em;font-weight:bold;letter-spacing:0.5px;font-style: italic">Bon appétit!</p>
</div>
<footer>

</footer>

<style>
.menu-header {
	margin: 10px;
	padding: 20px;
	background-image: url("https://images.unsplash.com/photo-1611601184963-9d1de9b79ff3?ixlib=rb-1.2.1&dl=davey-gravy-krsKfCC1lYw-unsplash.jpg&q=80&fm=jpg&crop=entropy&cs=tinysrgb");
	background-size: 250vh;
	background-repeat: no-repeat;
}
.menu-header_title {
	font-family: 'Playfair Display', serif;
	margin: 10px;
	padding: 1px;
	color: #fff;
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
    width:33%;
    float:left;
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
a {
	color: var(--accent-color);
	text-decoration: none;
}
a:hover {
	text-decoration: underline;
	color: blue;
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
	margin-left:20%;
}
.menu-list p span.droite {
	float: right;
	margin-right:20%;
}
.description {
	float: left;
	margin-left:20%;
}


</style>
