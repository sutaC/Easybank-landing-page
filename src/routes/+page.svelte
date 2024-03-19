<script lang="ts">
	import Articles from '$lib/sections/Articles.svelte';
	import Footer from '$lib/sections/Footer.svelte';
	import Header from '$lib/sections/Header.svelte';
	import Hero from '$lib/sections/Hero.svelte';
	import Information from '$lib/sections/Information.svelte';
</script>

<main>
	<Header></Header>
	<Hero></Hero>
	<Information></Information>
	<Articles></Articles>
	<Footer></Footer>

	<div class="attribution">
		Challenge by
		<a href="https://www.frontendmentor.io?ref=challenge" target="_blank" rel="noopener noreferrer"
			>Frontend Mentor</a
		>. Coded by
		<a href="https://github.com/sutaC" target="_blank" rel="noopener noreferrer">sutaC</a>.
	</div>
</main>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Public+Sans:ital,wght@0,100..900;1,100..900&display=swap');

	:global(:root) {
		/*
			| Primary
			> Dark Blue: hsl(233, 26%, 24%)
			> Lime Green: hsl(136, 65%, 51%)
			> Bright Cyan: hsl(192, 70%, 51%)
			| Neutral
			> Grayish Blue: hsl(233, 8%, 62%)
			> Light Grayish Blue: hsl(220, 16%, 96%)
			> Very Light Gray: hsl(0, 0%, 98%)
			>White: hsl(0, 0%, 100%)
        */
		--clr-text: hsl(233, 26%, 24%);
		--clr-primary: hsl(136, 65%, 51%);
		--clr-secondary: hsl(192, 70%, 51%);
		--clr-text-light: hsl(233, 8%, 62%);
		--clr-section-bg: hsl(220, 16%, 96%);
		--clr-body-bg: hsl(0, 0%, 98%);
		--clr-base: hsl(0, 0%, 100%);
		--fw-light: 300;
		--fw-normal: 400;
		--fw-bold: 700;
	}

	:global(*) {
		font-family: 'Public Sans', sans-serif;
		box-sizing: border-box;
	}

	:global(html) {
		font-family: 'Public Sans', sans-serif;
		font-size: 18px;
		font-weight: var(--fw-normal);
		color: var(--clr-text);
	}

	:global(body) {
		margin: 0;
		min-height: 100vh;
		background-color: var(--clr-body-bg);
	}

	/* --- */

	:global(.mobile) {
		display: block;
	}
	:global(.desktop) {
		display: none;
	}
	@media (width >= 700px) {
		:global(.mobile) {
			display: none;
		}
		:global(.desktop) {
			display: block;
		}
	}

	/* --- */

	.attribution {
		padding: 0.125rem;
		width: 100%;
		position: fixed;
		left: 0;
		bottom: 0;
		font-size: 0.65rem;
		text-align: center;
		color: var(--clr-text-light);
	}

	.attribution a {
		color: var(--clr-secondary);
		transition: opacity 100ms ease-in-out;
	}

	.attribution :where(a:hover, a:focus) {
		opacity: 0.75;
	}
</style>
