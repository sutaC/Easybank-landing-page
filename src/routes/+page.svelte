<script lang="ts">
	import Header from '$lib/sections/Header.svelte';
	import Hero from '$lib/sections/Hero.svelte';
	import Information from '$lib/sections/Information.svelte';
</script>

<main>
	<Header></Header>
	<Hero></Hero>
	<Information></Information>
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
</style>
