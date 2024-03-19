<script lang="ts">
	import CustomButton from '$lib/components/CustomButton.svelte';

	let dialog: HTMLDialogElement | null = null;

	function handleOpenNav() {
		dialog?.showModal();
	}

	function handleCloseNav() {
		dialog?.close();
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

	<button class="hamburger mobile" aria-label="Open navigation" on:click={handleOpenNav}>
		<img src="/images/icon-hamburger.svg" alt="Hamburger" />
	</button>

	<div class="desktop">
		<CustomButton>Request Invite</CustomButton>
	</div>
</header>

<nav class="mobile">
	<dialog bind:this={dialog}>
		<a href="# " on:click={handleCloseNav}>Home</a>
		<a href="# " on:click={handleCloseNav}>About</a>
		<a href="# " on:click={handleCloseNav}>Contact</a>
		<a href="# " on:click={handleCloseNav}>Blog</a>
		<a href="# " on:click={handleCloseNav}>Careers</a>
	</dialog>
	<div class="backdrop"></div>
</nav>

<style>
	header {
		position: sticky;
		top: 0;
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

	dialog {
		border: none;
		border-radius: 0.5rem;
		width: 100%;
		top: -35%;
	}

	dialog::backdrop {
		background: transparent;
	}

	.backdrop {
		display: none;
	}

	dialog[open] + .backdrop {
		display: block;
		position: fixed;
		left: 0;
		top: 0;
		width: 100vw;
		height: 100vh;
		background: linear-gradient(var(--clr-text), transparent);
	}

	nav a {
		display: block;
		text-decoration: none;
		color: var(--clr-text);
		text-align: center;
		font-weight: var(--fw-light);
		transition: all 150ms ease-out;
	}

	nav a:hover {
		opacity: 0.7;
	}

	dialog > a {
		margin: 1rem;
	}

	@media (width >= 700px) {
		nav.desktop {
			display: flex;
			gap: 1rem;
		}
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

	dialog[open],
	.backdrop {
		animation: fadeIn 150ms ease-out;
	}

	@media (width > 700px) {
		header {
			justify-content: space-evenly;
		}
	}
</style>
