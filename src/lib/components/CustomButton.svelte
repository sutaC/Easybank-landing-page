<button on:click>
	<slot />
</button>

<style>
	button {
		padding: 1em 2em;
		border: none;
		border-radius: 2rem;
		background: linear-gradient(to right, var(--clr-primary), var(--clr-secondary));
		font-size: 0.75rem;
		font-weight: var(--fw-nromal);
		color: var(--clr-base);
		text-align: center;
	}
</style>
