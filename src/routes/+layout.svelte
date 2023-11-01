<script>
</script>

<div class="container">
	<header>
		<div id="logo">Faik Yesilyaprak</div>

		<nav>
			<a href="#"> Home </a>

			<a href="#"> Projects </a>

			<a href="#"> About Me </a>

			<a href="#"> FAQs </a>
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
		gap: calc(16px + 1vw);
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
		justify-content: space-around;
		align-items: center;
		width: 100%;
		height: 100%;
	}

	a {
		font-weight: 700;
	}

	main {
		/* background: blue; */
		grid-column: 2/12;
	}

	#logo {
		/* background: yellow; */
		width: 100%;
		height: 100%;

		display: flex;
		align-items: center;
		font-size: 2rem;
	}

	footer {
		display: flex;
		justify-content: center;
		align-items: center;
		margin: 1rem;
	}
</style>
