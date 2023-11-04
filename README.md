# Skeleton Responsive UI with Svelte

Welcome to the Skeleton Responsive UI project using Svelte! This project provides a responsive layout template that you can use as a starting point for your web applications. It's designed to be clean, minimal, and adaptable to various screen sizes and devices.

🚀 **Getting Started**

To get started with this project, follow these simple steps:

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/FaikYY/svelte-skeleton.git
   ```

2. Change into the project directory:

   ```bash
   cd your-svelte-skeleton
   ```

3. Install the necessary dependencies:

   ```bash
   npm install
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

5. Open your web browser and navigate to [http://localhost:5173](http://localhost:5173) to see the responsive UI in action.

🌟 **Features**

- Responsive grid layout with 12 columns.
- A navigation bar with links to Home, Projects, About Me, and FAQs.
- Clean and minimalistic design.
- Designed to work on various screen sizes.
- Sticky header for easy navigation.

📄 **Layout Structure**

The layout structure is defined in the `layout.svelte` file. It includes the following sections:

- Header with a navigation bar.
- Main content area.
- Footer with a creator's credit.

```html
<script>
	import { page } from '$app/stores';
</script>

<div class="container">
	<header>
		<div id="logo">Your Name</div>

		<nav>
			<a href="/" aria-current={$page.url.pathname === '/' ? 'page' : undefined}> Home </a>
			<a href="projects" aria-current={$page.url.pathname === '/projects' ? 'page' : undefined}> Projects </a>
			<a href="about" aria-current={$page.url.pathname === '/about' ? 'page' : undefined}> About Me </a>
			<a href="faqs" aria-current={$page.url.pathname === '/faqs' ? 'page' : undefined}> FAQs </a>
		</nav>
	</header>

	<main>
		<slot />
		<footer>Created by Faik Yesilyaprak with ❤️ 🧠</footer>
	</main>
</div>
```

🎨 **Customization**

You can easily customize this template to fit your project's needs. Modify the colors, add your logo, and adjust the navigation links to match your content.

📝 **License**

This project is licensed under the [MIT License](LICENSE).

📬 **Contact**

If you have any questions or suggestions, feel free to contact the project creator:

- [Email](mailto:faikyesilyaprak@outlook.com)
- [GitHub](https://github.com/FaikYY)
- [Twitter/ X.com](https://twitter.com/Faik_YY)

Happy coding! 🚀👨‍💻🎉
