<script>
	import CustomButton from '$lib/components/CustomButton.svelte';
</script>

<footer>
	<div class="wrapper">
		<div class="collumn">
			<a href="# " class="logo">
				<img src="/images/logo.svg" alt="Logo" />
			</a>

			<div class="socials">
				<a
					href="http://facebook.com"
					target="_blank"
					rel="noopener noreferrer"
					style="--_icon: url('/images/icon-facebook.svg')"
					aria-label="Facebook"
				>
				</a>
				<a
					href="http://youtube.com"
					target="_blank"
					rel="noopener noreferrer"
					style="--_icon: url('/images/icon-youtube.svg')"
					aria-label="YouTube"
				>
				</a>
				<a
					href="http://twitter.com"
					target="_blank"
					rel="noopener noreferrer"
					style="--_icon: url('/images/icon-twitter.svg')"
					aria-label="Twitter"
				>
				</a>
				<a
					href="http://pinterest.com"
					target="_blank"
					rel="noopener noreferrer"
					style="--_icon: url('/images/icon-pinterest.svg')"
					aria-label="Pinterest"
				>
				</a>
				<a
					href="http://instagram.com"
					target="_blank"
					rel="noopener noreferrer"
					style="--_icon: url('/images/icon-instagram.svg')"
					aria-label="Instagram"
				>
				</a>
			</div>
		</div>

		<div class="links">
			<a href="# ">About Us</a>
			<a href="# ">Contact</a>
			<a href="# ">Blog</a>
			<a href="# ">Careers</a>
			<a href="# ">Support</a>
			<a href="# ">Privacy Policy</a>
		</div>
	</div>

	<div class="collumn">
		<div class="btnContainer">
			<CustomButton>Request Invite</CustomButton>
		</div>

		<small class="copyright">© Easybank. All Rights Reserved</small>
	</div>
</footer>

<style>
	footer {
		padding: 1.75rem;
		background-color: var(--clr-text);
		color: var(--clr-base);
		text-align: center;
	}

	footer > * {
		margin: 1.75rem auto;
	}

	a {
		display: block;
		color: var(--clr-base);
		text-decoration: none;
		font-size: 0.8rem;
	}

	.logo {
		background-color: color-mix(in srgb, white 20%, transparent 100%);
		width: fit-content;
		margin: auto;
		padding: 0.2rem;
		border-radius: 2rem;
		display: grid;
		place-content: center;
		margin: 1.75rem auto;
	}

	.socials {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 1rem;
	}

	.socials a {
		width: 1rem;
		aspect-ratio: 1;
		background-color: var(--clr-base);
		display: block;
		mask-image: var(--_icon);
		mask-size: cover;
		mask-position: center;
		mask-repeat: no-repeat;
		z-index: 0;
		transition: all 150ms ease-out;
	}

	.socials a:where(:hover, :active) {
		background-color: var(--clr-primary);
	}

	.links a {
		margin: 1rem 0;
		transition: all 150ms ease-out;
	}

	.links a:where(:hover, :active) {
		color: var(--clr-primary);
	}

	.btnContainer {
		margin: 1.75rem auto;
	}

	.copyright {
		color: var(--clr-text-light);
		font-size: 0.75rem;
	}

	@media (width >= 800px) {
		footer,
		.wrapper {
			display: flex;
			justify-content: space-between;
			align-items: center;
		}

		footer {
			padding-inline: 5%;
		}

		.wrapper {
			gap: 4rem;
		}

		.collumn {
			display: flex;
			justify-content: center;
			flex-direction: column;
			gap: 2rem;
		}

		footer > *,
		.collumn > * {
			margin: 0;
		}

		.btnContainer {
			text-align: right;
		}

		.links {
			display: grid;
			grid-template-columns: repeat(2, 1fr);
			gap: 1rem 4rem;
		}

		.links a {
			margin: 0;
			text-align: left;
		}
	}
</style>
