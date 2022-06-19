<script src="/Users/vincentdevillard/Desktop/SvelteKit/node_modules/require">

import deepai from 'deepai'

		deepai.setApiKey('4fcf05e9-845f-4838-9323-1d60606ff713');

		(async function() {
			var resp = await deepai.callStandardApi("text-generator", {
					text: "The values of our brunch restaurant are",
			});
			console.log(resp)
		})()

</script>

<div class="main">	

			<div class="description2">    
			</div>	
				
			</div> 

			<div class="description3">
				<p> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vulputate gravida lobortis. Ut sapien lacus, vestibulum quis lacinia ut, imperdiet ac est. Sed ex elit, lobortis nec nunc eget, fermentum interdum lacus. Donec faucibus volutpat quam, ornare elementum dui imperdiet sit amet. Mauris sed convallis magna. Vestibulum ut elit id ex suscipit auctor et vel neque. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam posuere volutpat lectus, id tincidunt tellus facilisis non. Sed risus nibh, imperdiet ut mi sit amet, dignissim tristique dolor. Aenean sodales ante nec odio ullamcorper, fringilla semper nunc commodo.
				</p>
			</div> 


<style>


	.description2 {
		position: absolute;
		top: 95%;
		right: 5%;
		left: 40%;
		background-color: rgba(0, 0, 0, 0.661);
		color: white;
		padding-left: 20px;
		padding-right: 20px;
	}

	.description3 {
		position: absolute;
		top: 160%;
		left: 15%;
		right: 30%;
		background-color: rgba(0, 0, 0, 0.661);
		color: white;
		padding-left: 20px;
		padding-right: 20px;
	}

	p {
		color: rgb(0, 0, 0);
		font-size: 2vmin;
	}

</style>