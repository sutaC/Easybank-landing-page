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
		cursor: pointer;
		transition: all 100ms ease-out;
	}

	button:where(:hover, :active) {
		background-color: rgba(255, 255, 255, 0.25);
		background-blend-mode: hard-light;
	}

	button:active {
		scale: 0.975;
	}
</style>
