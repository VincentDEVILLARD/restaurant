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

	import { Parallax, ParallaxLayer } from 'svelte-parallax';
	import Gallery from 'svelte-image-gallery'

</script>

<div class="main">	

	<Parallax sections={2} config={{stiffness: 0.3, damping: 0.3}}>

		<ParallaxLayer rate={-0.5} offset={0}>

			<Gallery gap=10>
				<img src="https://media.gettyimages.com/photos/women-eating-fresh-mediterranean-platter-on-table-picture-id1224986971?k=20&m=1224986971&s=612x612&w=0&h=dNDRNIKQqmOWxHNXwwxz8zo-DR_7rvpO1-50hqG6g1s=" alt="">
				<img src="https://media.gettyimages.com/photos/variety-of-healthy-toasts-with-vegetables-seeds-and-microgreens-picture-id1306631277?k=20&m=1306631277&s=612x612&w=0&h=1f6dgdhpttBTyXImyP8JUxPgDBhoWdvwj424S-Y0CzE=" alt="">
				<img src="https://media.gettyimages.com/photos/happy-business-owner-opening-the-door-at-a-cafe-wearing-a-facemask-picture-id1225861949?k=20&m=1225861949&s=612x612&w=0&h=yhIw9RcZ09VCayfI1E9UO72ifwll1KjPv3k0zW0Z9SA=" alt="">
				<img src="https://media.gettyimages.com/photos/sharing-food-picture-id1136787082?k=20&m=1136787082&s=612x612&w=0&h=-FpLLD69DH-2ADrPnERZQIQ_BsTmsGfrEcU9wTAPwXk=" alt="">
				<img src="https://media.gettyimages.com/photos/salmon-toast-and-cheese-cream-picture-id1206140040?k=20&m=1206140040&s=612x612&w=0&h=X6QqUu0LR8uijG_y3ueZLMzEiIymtEa3M8NvczAoOos=" alt="">
				<img src="https://media.gettyimages.com/photos/pan-fried-duck-picture-id1081422898?k=20&m=1081422898&s=612x612&w=0&h=YkfQqtV3nN1gB_HaehyvjcTEye7w9FBPkG-PIKdDzPo=" alt="">
				<img src="https://media.gettyimages.com/photos/cozy-restaurant-for-gathering-with-friends-picture-id1159992039?k=20&m=1159992039&s=612x612&w=0&h=t2lqevaWYLXvcjDeKzbHvIRF6GE3gxiqO6AIezr3Mws=" alt="">
				<img src="https://media.gettyimages.com/photos/luxury-restaurant-interior-at-night-picture-id1248298359?k=20&m=1248298359&s=612x612&w=0&h=hjiGlhw6CkX_YEgQUqKl8QmCDrFJ_OXyqdTqSDSNqy8=" alt="">
				<img src="https://media.gettyimages.com/photos/woman-having-food-at-restaurant-table-picture-id556561965?k=20&m=556561965&s=612x612&w=0&h=hyAY3BMhb9sk3rTR6mQBAfxfDr8pFaPhqMX1xZd0ztc=" alt="">
				<img src="https://media.gettyimages.com/photos/restaurant-eating-picture-id1178808772?k=20&m=1178808772&s=612x612&w=0&h=lV6WhUhQE99vDN7N1LSLQ30VLzlfI8I3CmdJSDcKZdU=" alt="">
				<img src="https://media.gettyimages.com/photos/friends-enjoying-a-meal-picture-id524296353?k=20&m=524296353&s=612x612&w=0&h=aeXpdk87ENZYazyG-bhZ58jfQGxS7g_O6aCU_WCT9-Q=" alt="">
				<img src="https://media.gettyimages.com/photos/cafebar-in-moscow-picture-id1158221681?k=20&m=1158221681&s=612x612&w=0&h=FXwKQ7jUKTv5dtBJ5xEPvz1IVhVTCEEBitr0yD2RNtc=" alt="">
				<img src="https://media.gettyimages.com/photos/closeup-of-waiter-walkiing-with-dishes-picture-id662284017?k=20&m=662284017&s=612x612&w=0&h=THkLZi5cYHYI6TtaPGxJVmA2vmH1GIg5teBnnyEDXJU=" alt="">
				<img src="https://media.gettyimages.com/photos/man-eating-freshly-prepared-meal-in-restaurant-picture-id1296353050?k=20&m=1296353050&s=612x612&w=0&h=nMXYYY7WiicdJ5Xv0zLH5uu-iLLARSF6plq4Q9DTtfk=" alt="">
				<img src="https://media.gettyimages.com/photos/an-empty-luxurious-restaurant-picture-id1209064521?k=20&m=1209064521&s=612x612&w=0&h=UGf7aIrjq5Ybv01kWFEUor4SjiX55rGR3ajmNBOj918=" alt="">
				<img src="https://media.gettyimages.com/photos/group-of-friends-eating-at-a-restaurant-picture-id1056925792?k=20&m=1056925792&s=612x612&w=0&h=OZvDjzL6srbjBtUtlWJe6IUGO5yMl-Krv-IQddayrNE=" alt="">
				<img src="https://media.gettyimages.com/photos/customer-receiving-food-at-burger-restaurant-picture-id1034323470?k=20&m=1034323470&s=612x612&w=0&h=mqzBpY1Ai_C05oEVCAzJyLOMgelkZJ1jcVsaxY9gPZc=" alt="">
				<img src="https://media.gettyimages.com/photos/sharing-food-picture-id825855446?k=20&m=825855446&s=612x612&w=0&h=GiaR3DFDYPFFaTV8FrBHVX1XJ8xfRt9AT3Eq5iGegjo=" alt="">
				<img src="https://media.gettyimages.com/photos/happy-business-owner-opening-the-door-at-a-cafe-wearing-a-facemask-picture-id1225861959?k=20&m=1225861959&s=612x612&w=0&h=H0hMfUJlbThEU1O20CYn2IRRXZMMSYG0SyXW3rGUUBA=" alt="">
				<img src="https://media.gettyimages.com/photos/multi-generational-family-in-a-cafe-picture-id1095217166?k=20&m=1095217166&s=612x612&w=0&h=Hbhu_p26i8-vRfoYcLpb3a-9J7rHxyX7w1TCO9ISJ0c=" alt="">
				<img src="https://media.gettyimages.com/photos/rendering-of-a-luxury-restaurant-interior-at-night-picture-id1248298343?k=20&m=1248298343&s=612x612&w=0&h=ds0WoCXpF4qesggrtYk6nPtZyCBxegzmVPyW2KBzhy4=" alt="">
				<img src="https://media.gettyimages.com/photos/enjoying-food-picture-id1158741311?k=20&m=1158741311&s=612x612&w=0&h=m8Hl0baj23-yb4yfG5h_8zN-CXAHe7f9yeRwWqw7ajc=" alt="">
				<img src="https://media.gettyimages.com/photos/brunch-for-two-people-at-the-cafe-high-angle-view-picture-id1025838484?k=20&m=1025838484&s=612x612&w=0&h=5dbuqR_sR26fGnW1aX-Biy7pxPqviLNd49cdR9fPecM=" alt="">
				<img src="https://media.gettyimages.com/photos/friends-eating-at-a-restaurant-picture-id693186850?k=20&m=693186850&s=612x612&w=0&h=0AxHX1ONb9h99BV5K9snxp0Xj7wC3T4pUG4ZJpddGq0=" alt="">
				<img src="https://media.gettyimages.com/photos/friends-enjoying-brunch-picture-id1136787445?k=20&m=1136787445&s=612x612&w=0&h=i89MyvHFrjwyv0U9G_CX7M18J9Go_yudvgJAdOMg3xs=" alt="">
				<img src="https://media.gettyimages.com/photos/waitress-at-a-restaurant-getting-a-delivery-order-on-the-phone-and-a-picture-id1256186622?k=20&m=1256186622&s=612x612&w=0&h=BBt6cHgbVZGob5knjRH9xwwwipSiJAbcFyj8eOxyNYI=" alt="">
				<img src="https://media.gettyimages.com/photos/chef-serving-food-picture-id1158191245?k=20&m=1158191245&s=612x612&w=0&h=JI5SuS-TfQUY5lkdPBtIMMDDATRwUGc8RpaI5RWDHBI=" alt="">
				<img src="https://media.gettyimages.com/photos/contactless-payment-in-a-coffee-shop-picture-id1180768785?k=20&m=1180768785&s=612x612&w=0&h=Xjdnj9OzzNOyo64EuW1N9RjsQyeAU9MOP9sZMcs8rug=" alt="">
				<img src="https://media.gettyimages.com/photos/group-of-joyful-young-asian-man-and-woman-having-fun-enjoying-food-picture-id1155378580?k=20&m=1155378580&s=612x612&w=0&h=iu-evMB3NSUhLVjMDmJJFszk1syHtK70Ixn0e8DyyW0=" alt="">
				<img src="https://media.gettyimages.com/photos/laughing-friends-in-restaurant-eating-dessert-picture-id518495009?k=20&m=518495009&s=612x612&w=0&h=cidfPbPjiobUehnRe_JcXE99-TmSbD36ogqS1tjOQDQ=" alt="">
				<img src="https://media.gettyimages.com/photos/chef-preparing-a-flambe-dish-at-gas-stove-in-restaurant-kitchen-picture-id1205077625?k=20&m=1205077625&s=612x612&w=0&h=Ndp3O-xKrUOMKarO_oNCoHs5xKJudmsu8w0dz9wiKUQ=" alt="">
				<img src="https://media.gettyimages.com/photos/chef-preparing-dish-in-kitchen-picture-id137737392?k=20&m=137737392&s=612x612&w=0&h=0NkEp9EWrGKpKRvKTXRkrRP61s7B5rH_fnT6PgB3_Q8=" alt="">
				<img src="https://media.gettyimages.com/photos/service-thats-friendly-and-hygienic-picture-id1281800137?k=20&m=1281800137&s=612x612&w=0&h=yPGF-z0szZ69KjDJFKF8Q10i1aI6-eIkvoZFbHxtaYc=" alt="">
				<img src="https://media.gettyimages.com/photos/cheers-picture-id1136788675?k=20&m=1136788675&s=612x612&w=0&h=x38zIrHGcf7FwjzqyTY4mrlQ3tr72iSdc74V_Aarj_8=" alt="">
				<img src="https://media.gettyimages.com/photos/busy-bar-scene-picture-id524578461?k=20&m=524578461&s=612x612&w=0&h=zYFvdZW7Uledt1JZ2sCWjNdrCQ0JnaMUIkrzK3gnwVM=" alt="">
			</Gallery>


		</ParallaxLayer>

		<ParallaxLayer rate={-0.25} offset={0}>	
			 <!--C'est pas la version finale, l'idée c'est d'avoir plusieurs petits aliments qui se baladent-->
			<img src="/img/backgroundbrunch.png" alt="" width=100%>
		</ParallaxLayer>

		<ParallaxLayer rate={0} offset={0}>	
			<div class="description1">
				<p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vulputate gravida lobortis. Ut sapien lacus, vestibulum quis lacinia ut, imperdiet ac est. Sed ex elit, lobortis nec nunc eget, fermentum interdum lacus. Donec faucibus volutpat quam, ornare elementum dui imperdiet sit amet. Mauris sed convallis magna. Vestibulum ut elit id ex suscipit auctor et vel neque. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam posuere volutpat lectus, id tincidunt tellus facilisis non. Sed risus nibh, imperdiet ut mi sit amet, dignissim tristique dolor. Aenean sodales ante nec odio ullamcorper, fringilla semper nunc commodo.

					Mauris ut efficitur nibh. Morbi vestibulum varius metus, vel sagittis orci aliquet vitae. Vivamus ipsum dui, cursus non magna ut, tempor euismod tortor. Vestibulum elementum non neque vitae mattis. Etiam sed maximus metus, et efficitur quam. Nunc mauris felis, gravida ut tortor non, luctus sollicitudin libero. Sed mollis efficitur nibh non iaculis. Aenean efficitur malesuada dui, a pretium diam gravida sed. Cras ultrices finibus velit, sit amet consequat nulla commodo eu. Maecenas vestibulum ultrices leo eu rutrum. Phasellus sed massa sit amet lorem malesuada congue. Sed eget placerat neque, ut varius ante. 
				</p>
			</div> 
			<div class="description2">
				<p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vulputate gravida lobortis. Ut sapien lacus, vestibulum quis lacinia ut, imperdiet ac est. Sed ex elit, lobortis nec nunc eget, fermentum interdum lacus. Donec faucibus volutpat quam, ornare elementum dui imperdiet sit amet. Mauris sed convallis magna. Vestibulum ut elit id ex suscipit auctor et vel neque. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam posuere volutpat lectus, id tincidunt tellus facilisis non. Sed risus nibh, imperdiet ut mi sit amet, dignissim tristique dolor. Aenean sodales ante nec odio ullamcorper, fringilla semper nunc commodo.

					Mauris ut efficitur nibh. Morbi vestibulum varius metus, vel sagittis orci aliquet vitae. Vivamus ipsum dui, cursus non magna ut, tempor euismod tortor. Vestibulum elementum non neque vitae mattis. Etiam sed maximus metus, et efficitur quam. Nunc mauris felis, gravida ut tortor non, luctus sollicitudin libero. Sed mollis efficitur nibh non iaculis. Aenean efficitur malesuada dui, a pretium diam gravida sed. Cras ultrices finibus velit, sit amet consequat nulla commodo eu. Maecenas vestibulum ultrices leo eu rutrum. Phasellus sed massa sit amet lorem malesuada congue. Sed eget placerat neque, ut varius ante. 
				</p>
			</div> 
			<div class="description3">
				<p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vulputate gravida lobortis. Ut sapien lacus, vestibulum quis lacinia ut, imperdiet ac est. Sed ex elit, lobortis nec nunc eget, fermentum interdum lacus. Donec faucibus volutpat quam, ornare elementum dui imperdiet sit amet. Mauris sed convallis magna. Vestibulum ut elit id ex suscipit auctor et vel neque. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam posuere volutpat lectus, id tincidunt tellus facilisis non. Sed risus nibh, imperdiet ut mi sit amet, dignissim tristique dolor. Aenean sodales ante nec odio ullamcorper, fringilla semper nunc commodo.

					Mauris ut efficitur nibh. Morbi vestibulum varius metus, vel sagittis orci aliquet vitae. Vivamus ipsum dui, cursus non magna ut, tempor euismod tortor. Vestibulum elementum non neque vitae mattis. Etiam sed maximus metus, et efficitur quam. Nunc mauris felis, gravida ut tortor non, luctus sollicitudin libero. Sed mollis efficitur nibh non iaculis. Aenean efficitur malesuada dui, a pretium diam gravida sed. Cras ultrices finibus velit, sit amet consequat nulla commodo eu. Maecenas vestibulum ultrices leo eu rutrum. Phasellus sed massa sit amet lorem malesuada congue. Sed eget placerat neque, ut varius ante. 
				</p>
			</div> 
		</ParallaxLayer>

	</Parallax>
</div>

<style>

	.description1 {
		position: absolute;
		top: 20%;
		left: 5%;
		right: 40%;
		background-color: rgba(0, 0, 0, 0.661);
		color: white;
		padding-left: 20px;
		padding-right: 20px;
	}

	.description2 {
		position: absolute;
		top: 80%;
		right: 5%;
		left: 40%;
		background-color: rgba(0, 0, 0, 0.661);
		color: white;
		padding-left: 20px;
		padding-right: 20px;
	}


	.description3 {
		position: absolute;
		top: 140%;
		left: 15%;
		right: 30%;
		background-color: rgba(0, 0, 0, 0.661);
		color: white;
		padding-left: 20px;
		padding-right: 20px;
	}

	p {
		color: white;
	}

</style>