<script>
	import { page } from '$app/stores';
</script>

<header>
	<div class="corner">
		<a href="/homepage">
			<img src="/img/LogoRB.png" alt="">
		</a>
	</div>

	<nav>

		<ul>
			<li class:active={$page.url.pathname === '/homepage'}>
				<a sveltekit:prefetch href="/homepage">Home</a>
			</li>
			<li class:active={$page.url.pathname === '/history'}>
				<a sveltekit:prefetch href="/history">About Us</a> 
			</li>	
			<li class:active={$page.url.pathname === '/menu'}>
				<a sveltekit:prefetch href="/menu">Menu</a> 
			</li>
			<li class:active={$page.url.pathname === '/recruitments'}>
				<a sveltekit:prefetch href="/recruitments">Recruitments</a>
			</li>
			<li class:active={$page.url.pathname === '/ourTeam'}>
				<a sveltekit:prefetch href="/ourTeam">The Team</a>
			</li>
			<li class:active={$page.url.pathname === '/privatisation-reservation'}>
				<a sveltekit:prefetch href="/privatisation-reservation">Book a Table</a>
			</li>
		</ul>

	</nav>

</header>



<style>
	header {
		display: flex;
		justify-content: space-between;
		background-color: white;
	}

	.corner {
		width: 11em;
		height: 3em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
	}

	img {
		height: 50px;
	}

	nav {
		display: flex;
		justify-content: right;
		--background: rgb(255, 255, 255);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li.active::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(black);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--heading-color);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--accent-color);
	}
</style>
