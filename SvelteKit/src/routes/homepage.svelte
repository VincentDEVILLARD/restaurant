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
	<meta name="description" content="Refresh Brunch - Homepage" />
</svelte:head>

<div class=Video>
	<video autoplay muted loop class="Video">
		<source src="/videohomepage.mp4" type="video/mp4">
	</video>
	<div class="caption">
		<h3>Refresh Brunch</h3>
		<h4>Fresh & French food. Cooked with love in Cergy. Brunch, Tapas and more...</h4>
	</div>
</div>

<div class="main">	

		<main class="Carousel">

			<div class="container">
			 
			  <div class="slideshow">
				<div class="box">
				  <a href='./history'><img src="/img/kousbi1.jpg" alt=""></a>
				  <span>The Restaurant</span>>
				</div>
				<div class="box">
				  <a href='./ourTeam'><img src="/img/kousbi2.png" alt=""></a>
				  <span>The Team</span>
				</div>
				<div class="box">
				  <a href='./menu'><img src="/img/kousbi3.png" alt=""></a>
				  <span>The Food</span>
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
		font-size: 15vh;
		font-family: 'Times New Roman', Times, serif;
		text-shadow: 2px 2px black;
	}

	h4 {
		color:#ffffff;
		font-size: 3vh;
		font-family: 'Times New Roman', Times, serif;
		text-shadow: 1px 1px black;
	}


.container {
	width: 100%;
	padding-right: 15px;
	padding-left: 15px;
	margin-right: auto;
	margin-left: auto; 
}


.slideshow {
    display: flex;
    width: 100%;
    padding: 4% 2%;
    box-sizing: border-box;
    height: 100vh;
}
  
.box {
    flex: 1;
    overflow: hidden;
    transition: .5s;
    margin: 0 2%;
    line-height: 0;
	font-family: 'Times New Roman', Times, serif;
}
  
.box > a > img {
    width: 200%;
    height: calc(100% - 10vh);
    object-fit: cover; 
    transition: .5s;
}
  
.box > span {
    font-size: 3.8vh;
    display: block;
    text-align: center;
    height: 10vh;
    line-height: 2.6;
}
  
.box:hover { flex: 1 1 50%; }
  .box:hover > a > img {
    width: 100%;
    height: 100%;
}
</style>