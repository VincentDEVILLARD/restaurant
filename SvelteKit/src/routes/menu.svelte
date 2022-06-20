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
			<a href="#drinks"><div class="colonne3"><h2>Drinks</h2></div></a>
			<br>
			<br>
			<br>
        	<div class="hline"></div>
    </div>
<div class="menu-list">
    <!--Ajouter scroll navigation pour pas de défilement-->
    <br/><br/>
	<h2 class="menu-list_title" id="brunch">Brunch (10h-15h)</h2>
    <div class="brunchpic"></div>
    <div class="vline"></div>
		<h3 class="menu-list_subcategory">Salted</h3>	
		<div>
		    <!-- Liste menu brunch salé - petites faims -->
			<h4 class="menu-list_subcategory2">Salted - Little Hunger</h4>
			<div>
                <p><span class="gauche" style="font-weight: bold">Avocado Toast</span><span class="droite" style="font-style:italic;color:grey">8€</span></p><br/>
                <div class="description">Avocado mash on toasted
					sourdough with herb oil, chili
					flakes, pickled red onion,
					chives, seedse</div><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Eggs Benedicte</span><span class="droite" style="font-style:italic;color:grey">9€</span></p><br/>
                <div class="description">Honey roasted gammon ham, poached organic eggs, homemade hollandaise sauce on toasted organic muffins</div><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Bagel & Salmon</span><span class="droite" style="font-style:italic;color:grey">9€</span></p><br/>
                <div class="description">Toasted bagel, smoked salmon, chive cream cheese, pickled onions, sliced tomato, mixed salad, lemon wedge</div><br/>
			</div>
            <div class="vline"></div>
				<!--Liste menu brunch salé - grandes faims-->
				<h4 class="menu-list_subcategory2">Salted - Big Hunger</h4>
				<div style="font-weight:lighter; font-style:italic; margin: 0 20% 0 20%">All with fried potatoes, mushrooms, house baked beans, roasted tomatoes, tomato jam,toast & butter. Choose below:</div><br/>
			<div>
                <p><span class="gauche" style="font-weight: bold">Avocado Refresh Plate</span><span class="droite" style="font-style:italic;color:grey">15,9€</span></p><br/>
                <div class="description">Avocado & 2 eggs your way</div><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Bacon Refresh Plate</span><span class="droite" style="font-style:italic;color:grey">16,9€</span></p><br/>
                <div class="description">Bacon & 2 eggs your way</div><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Vegan Refresh Plate</span><span class="droite" style="font-style:italic;color:grey">14,9€</span></p><br/>
                <div class="description">Scrambled tofu & veggie sausage</div><br/>
			</div>
		</div>
        <div class="vline"></div>
		<h3 class="menu-list_subcategory">Sweet</h3><br/>
		<div>
			<!--Liste menu brunch sucré-->
			<div>
                <p><span class="gauche" style="font-weight: bold">Fluffy Pancakes</span><span class="droite" style="font-style:italic;color:grey">4,5€ / 6,5€ / 7,5€</span></p><br/>
                <div class="description">3 American pancakes - Choice of fillings, depending on the season (1 filling / 2 fillings): chocolate, banana, raspberry, maple syrup, whipped cream, jam, honey, lemon, coconut</div><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Acai Bowl</span><span class="droite" style="font-style:italic;color:grey">7,5€</span></p><br/>
                <div class="description">Creamy frozen smoothie bowl with house made nutty granola, fresh berries, fruit & toasted coconut</div><br/><br/><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Muesli Bowl</span><span class="droite" style="font-style:italic;color:grey">6,5€</span></p><br/>
                <div class="description">Oat and quinoa bircher muesli with strawberry & apple, topped with whipped coconut cream</div><br/><br/><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Fruit Bowl</span><span class="droite" style="font-style:italic;color:grey">5,5€</span></p><br/>
                <div class="description">Freshly cut fruit of the day, please inform us of any allergies</div><br/><br/><br/>
			</div>
		</div>

	<h2 class="menu-list_title" id="tapas">Tapas (18h-00h)</h2>
    <div class="tapaspic"></div>
    <div class="vline"></div>
		<!--Liste menu tapas - plateaux découvertes-->
		<div>
			<h3 class="menu-list_subcategory">Discovery (2 persons)</h3>	
			<div>
                <p><span class="gauche" style="font-weight: bold">The big sharing board</span><span class="droite" style="font-style:italic;color:grey">21€</span></p><br/>
                <div class="description">All your favourite nibbles to share, Serrano ham and other charcuteries, grated tomatoes, marinated olives, salted almonds, French cheeses, chips, guacamole and hummus.</div><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Medium sharing board</span><span class="droite" style="font-style:italic;color:grey">16€</span></p><br/>
                <div class="description">French and Italian charcuteries, French cheese and bread with tomato or garlic bread</div><br/>
			</div>
		</div>
		<!--Liste menu tapas - petites portions-->
		<div>
            <div class="vline"></div>
			<h3 class="menu-list_subcategory">Small Bites</h3>	
			<div>
                <p><span class="gauche" style="font-weight: bold">Cheese Board</span><span class="droite" style="font-style:italic;color:grey">11€</span></p><br/>
                <div class="description">Mix of 4 French cheese of your choosing, with homemade bread: comté, tomme de brebis, chèvre frais, reblochon, saint-nectaire, rocamadour, camembert</div><br/>
				<br/>
				<p><span class="gauche" style="font-weight: bold">Breaded sheep's croquettes with honey</span><span class="droite" style="font-style:italic;color:grey">6€</span></p><br/>
                <div class="description">Served with salad</div><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Bread with tomato</span><span class="droite" style="font-style:italic;color:grey">4€</span></p><br/>
                <div class="description">3 slices</div><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Garlid Bread</span><span class="droite" style="font-style:italic;color:grey">4€</span></p><br/>
                <div class="description">3 slices</div><br/>
				<br/>
                <p><span class="gauche" style="font-weight: bold">Mini mixed salad</span><span class="droite" style="font-style:italic;color:grey">6,5€</span></p><br/>
                <div class="description">Choice of 3 ingredients: lettuce, radish, corn, tomato, sun-dried tomato, avocado, pumpkin seeds, carrot, edamame</div>
				<div class="description" style="margin-top:-1.5em">Protein supplement: 1,5€ each: mozzarella, chicken, anchovies, tofu</div><br/>

			</div>
		</div>
		<!--Liste menu tapas - desserts-->
		<div>
            <div class="vline"></div>

			<h3 class="menu-list_subcategory">Desserts</h3>	
			<p><span class="gauche" style="font-weight: bold">Fluffy Pancakes</span><span class="droite" style="font-style:italic;color:grey">4,5€ / 6,5€ / 7,5€</span></p><br/>
			<div class="description">3 American pancakes - Choice of fillings, depending on the season (1 filling / 2 fillings): chocolate, banana, raspberry, maple syrup, whipped cream, jam, honey, lemon, coconut</div><br/>
			<br/>
            <p><span class="gauche" style="font-weight: bold">Coulant au chocolat</span><span class="droite" style="font-style:italic;color:grey">4,5€</span></p><br/>
            <div class="description">Baked to order chocolate fondant with a hint of orange, served with clotted cream.</div><br/><br/><br/>
			<br/>
            <p><span class="gauche" style="font-weight: bold">Crème brulée</span><span class="droite" style="font-style:italic;color:grey">5,5€</span></p><br/>
            <div class="description">Classic vanilla</div><br/>
			<br/>		
            <p><span class="gauche" style="font-weight: bold">Pain perdu</span><span class="droite" style="font-style:italic;color:grey">5,5€</span></p><br/>
            <div class="description">French toast, coffee ice cream, bourbon whisky jelly and light honey mousse</div><br/><br/><br/>
			<br/>		
            <p><span class="gauche" style="font-weight: bold">Pour les gourmants</span><span class="droite" style="font-style:italic;color:grey">9€ (10€ with expresso)</span></p><br/>
            <div class="description">Mixed dessert plate for those that can't decide or are happy to share - a selection of our tasting desserts.</div><br/><br/><br/>
		</div>
        
	<h2 class="menu-list_title" id="drinks">Drinks</h2>
        <div class="drinkspic"></div>
        <div class="vline"></div>
		<!--Liste menu carte des boissons - sans alcool -->
		<div>
			<h3 class="menu-list_subcategory">Soft Drinks</h3>	
			<div>
                <p><span class="gauche" style="font-weight: bold">Freshly mixed fruit juice of the day</span><span class="droite" style="font-style:italic;color:grey">3,5€</span></p><br/><br/>

                <p><span class="gauche" style="font-weight: bold">Citronnade</span><span class="droite" style="font-style:italic;color:grey">3,5€</span></p><br/><br/>
			</div>
		</div>
		<!--Liste menu boissons chaudes-->
		<div>
            <div class="vline"></div>
			<h3 class="menu-list_subcategory">Hot Drinks</h3>	
            <p><span class="gauche" style="font-weight: bold">Expresso</span><span class="droite" style="font-style:italic;color:grey">1,5€</span></p><br/><br/>
            <p><span class="gauche" style="font-weight: bold">Americano</span><span class="droite" style="font-style:italic;color:grey">2€</span></p><br/><br/>
			<p><span class="gauche" style="font-weight: bold">Cappucino</span><span class="droite" style="font-style:italic;color:grey">3€</span></p><br/><br/>
			<p><span class="gauche" style="font-weight: bold">Lemon and Ginger Tea</span><span class="droite" style="font-style:italic;color:grey">2,5€</span></p><br/><br/>
			<p><span class="gauche" style="font-weight: bold">Green Tea</span><span class="droite" style="font-style:italic;color:grey">2€</span></p><br/><br/>
			<p><span class="gauche" style="font-weight: bold">Tea or Coffee "Gourmand"</span><span class="droite" style="font-style:italic;color:grey">10€ / 10,5€ / 10,5€</span></p><br/>
			<div class="description">Expresso, americano or green tee with mixed dessert plate for those that can't decide or are happy to share - a selection of our tasting desserts.</div><br/><br/><br/><br/>

		</div>
	</div>

</div>
<div>
    <p style="text-align: center;font-size: 1.2em;font-weight:bold;letter-spacing:0.5px;font-style: italic">Bon appétit!</p><br/>
	<div class="center">
		<a href="privatisation-reservation"><button class="button">Book a table</button></a>
	</div>
	<br/>
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
	text-align: center;
	display:table;
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
    display: inline-block;
    height: 0px;
    border: 0;
    border-top: 45px solid #ccc;
    margin: 0 0 0;
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
	margin-left:20%;
	margin-right:20%;
	float:left;
	font-weight: lighter;
	padding-bottom:1.5em;
	padding-top:0.5em;
}
/*.description {
	float: left;
	margin-left:20%;
	margin-right:20%;
	word-wrap: break-word;
}*/
.brunchpic {
    background-image: url(https://images.unsplash.com/photo-1522248105696-9625ba87de6e?ixlib=rb-1.2.1&dl=cera-SxTlB4fde9Q-unsplash.jpg&q=80&fm=jpg&crop=entropy&cs=tinysrgb);
    background-size:cover;
    background-repeat: no-repeat;
    background-position-y: -80px;
    height:30px;
	margin-left: 20%;
	margin-right: 20%;
    padding: 50px;
}
.tapaspic {
    background-image: url(https://images.unsplash.com/photo-1511357840105-748c95f0a7e7?ixlib=rb-1.2.1&dl=margherita-turrin-YUQEo7ajeLA-unsplash.jpg&q=80&fm=jpg&crop=entropy&cs=tinysrgb);
    background-size:cover;
    background-repeat: no-repeat;
    background-position-y: -40px;
    height:30px;
	margin-left: 20%;
	margin-right: 20%;
    padding: 50px;
}
.drinkspic {
    background-image: url(https://images.unsplash.com/photo-1563227812-0ea4c22e6cc8?ixlib=rb-1.2.1&dl=katherine-sousa-ln2R1wJ8TCM-unsplash.jpg&q=80&fm=jpg&crop=entropy&cs=tinysrgb);
    background-size:cover;
    background-repeat: no-repeat;
    background-position-y: -70px;
    height:30px;
	margin-left: 20%;
	margin-right: 20%;
    padding: 50px;
}
.center {
	display:flex;
	align-items: center;
  	justify-content: center;
}
.button {
  background-color: rgba(51, 51, 51, 0.05);
  border-radius: 8px;
  border-width: 0;
  color: #333333;
  cursor: pointer;
  display: inline-block;
  text-transform: uppercase;
  font-family: "Playfair Display", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 18px;
  font-weight: 500;
  line-height: 20px;
  list-style: none;
  /*margin: 10px 50% 30px ;*/
  padding: 10px 12px;
  text-align: center;
  transition: all 200ms;
  vertical-align: baseline;
  white-space: nowrap;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}
.button:hover {
  background-color: #ccc !important;
  color:rgb(48, 41, 29) !important; 
}

</style>
