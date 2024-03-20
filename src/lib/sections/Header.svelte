<script lang="ts">
	import CustomButton from '$lib/components/CustomButton.svelte';

	let dialog: HTMLDialogElement | null = null;
	let navOpen = false;

	function toggleNav() {
		navOpen = !navOpen;
	}
</script>

<header>
	<a href="/" class="logo">
		<img src="/images/logo.svg" alt="logo" />
	</a>

	<nav class="desktop">
		<a href="# ">Home</a>
		<a href="# ">About</a>
		<a href="# ">Contact</a>
		<a href="# ">Blog</a>
		<a href="# ">Careers</a>
	</nav>

	<button class="hamburger mobile" aria-label="Open navigation" on:click={() => toggleNav()}>
		{#if navOpen === true}
			<img src="/images/icon-close.svg" alt="Hamburger" />
		{:else}
			<img src="/images/icon-hamburger.svg" alt="Hamburger" />
		{/if}
	</button>

	<div class="desktop">
		<CustomButton>Request Invite</CustomButton>
	</div>
</header>

<nav class="mobile dialog" class:open={navOpen}>
	<a href="# " on:click={toggleNav}>Home</a>
	<a href="# " on:click={toggleNav}>About</a>
	<a href="# " on:click={toggleNav}>Contact</a>
	<a href="# " on:click={toggleNav}>Blog</a>
	<a href="# " on:click={toggleNav}>Careers</a>
</nav>

<div class="backdrop"></div>

<style>
	header {
		position: sticky;
		top: 0px;
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1rem;
		background-color: var(--clr-base);
		z-index: 100;
		isolation: isolate;
	}

	.hamburger {
		background-color: transparent;
		border: none;
	}

	.dialog {
		display: none;
	}

	.dialog.open {
		display: block;
		position: fixed;
		left: 50%;
		top: 30%;
		translate: -50% -50%;
		width: 90%;
		padding: 1rem;
		z-index: 95;
		border-radius: 0.5rem;
		background-color: var(--clr-base);
	}

	.backdrop {
		display: none;
	}

	.dialog.open + .backdrop {
		display: block;
		position: fixed;
		left: 0;
		top: 0;
		width: 100vw;
		height: 100vh;
		background: linear-gradient(var(--clr-text), transparent);
		z-index: 90;
	}

	:global(body):has(.dialog.open) {
		overflow: hidden;
	}

	nav a {
		display: block;
		text-decoration: none;
		color: var(--clr-text);
		text-align: center;
		font-weight: var(--fw-normal);
		transition: all 150ms ease-out;
	}

	nav a:hover {
		opacity: 0.7;
	}

	.dialog > a {
		margin: 1rem;
	}

	/* Animations */

	@keyframes fadeIn {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}

	.dialog.open,
	.backdrop {
		animation: fadeIn 150ms ease-out;
	}

	@media (width >= 800px) {
		header {
			justify-content: space-evenly;
		}

		nav.desktop {
			display: flex;
			gap: 2rem;
		}
	}
</style>
