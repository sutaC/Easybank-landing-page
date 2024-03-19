<script lang="ts">
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
	<button class="hamburger" aria-label="Open navigation" on:click={handleOpenNav}>
		<img src="/images/icon-hamburger.svg" alt="Hamburger" />
	</button>
</header>

<nav>
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

	dialog > a {
		display: block;
		text-decoration: none;
		color: var(--clr-text);
		text-align: center;
		margin: 1rem;
		font-weight: var(--fw-light);
		transition: all 150ms ease-out;
	}

	dialog > a:hover {
		opacity: 0.7;
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
</style>
