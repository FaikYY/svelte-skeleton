<script>
	import { page } from '$app/stores';
</script>

<div class="container">
	<header>
		<div id="logo__container">Faik Yesilyaprak</div>

		<nav>
			<a href="/" aria-current={$page.url.pathname === '/' ? 'page' : undefined}> Home </a>

			<a href="projects" aria-current={$page.url.pathname === '/projects' ? 'page' : undefined}>
				Projects
			</a>

			<a href="about" aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				About Me
			</a>

			<a href="faqs" aria-current={$page.url.pathname === '/faqs' ? 'page' : undefined}> FAQs </a>
		</nav>
	</header>

	<main>
		<slot />
		<footer>Created by Faik Yesilyaprak with ❤️ 🧠</footer>
	</main>
</div>

<style>
	.container {
		/* background: red; */
		gap: 2rem;
		display: grid;
		grid-template-columns: repeat(12, 1fr);
		grid-template-rows: calc(7.5vh + 7.5vw) 1fr;
		width: 100vw;
		height: 100%;
		min-height: 100%;
		box-sizing: border-box;
		overflow-x: hidden;
	}

	header {
		background-color: white;
		grid-column: 2/12;
		display: flex;
		justify-content: space-around;
		align-items: center;

		display: flex;
		flex-direction: column;

		position: sticky;
		top: 0;
	}

	nav {
		/*   background: purple; */
		display: flex;
		justify-content: center;
		column-gap: 2rem;
		flex-wrap: nowrap;
		align-items: center;
		width: 100%;
		height: 10%;
	}

	a {
		font-weight: 700;
	}

	main {
		/* background: blue; */
		grid-column: 2/12;
	}

	#logo__container {
		/* background: yellow; */
		width: 100%;
		height: 90%;

		display: flex;
		justify-content: center;
		align-items: center;
		font-size: 1.5rem;
		letter-spacing: 0.25rem;
		font-weight: 700;
	}

	footer {
		display: flex;
		justify-content: center;
		align-items: center;
		margin: 1rem;
	}

	@media (min-width: 1000px) {
		.container {
			grid-template-rows: calc(5vh + 5vw) 1fr;
		}

		nav {
			column-gap: 6rem;
		}
	}

	@media (min-width: 2000px) {
		#logo__container {
			height: 50%;
		}

		nav {
			height: 50%;
			align-items: flex-start;
		}
	}
</style>
