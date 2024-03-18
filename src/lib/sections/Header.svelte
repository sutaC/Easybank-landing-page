<script lang="ts">
	function handleOpenNav() {
		// TODO: handle it
	}
</script>

<header>
	<a href="/" class="logo">
		<img src="/images/logo.svg" alt="logo" />
	</a>
	<button class="hamburger" aria-label="Open navigation" on:click={() => handleOpenNav()}>
		<img src="/images/icon-hamburger.svg" alt="Hamburger" />
	</button>
</header>

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
</style>
