<script>
	import CustomButton from '$lib/components/CustomButton.svelte';
</script>

<footer>
	<a href="# " class="logo">
		<img src="/images/logo.svg" alt="Logo" />
	</a>

	<div class="socials">
		<a href="http://facebook.com" target="_blank" rel="noopener noreferrer">
			<img src="/images/icon-facebook.svg" alt="Facebook" />
		</a>
		<a href="http://youtube.com" target="_blank" rel="noopener noreferrer">
			<img src="/images/icon-youtube.svg" alt="YouTube" />
		</a>
		<a href="http:///twitter.com" target="_blank" rel="noopener noreferrer">
			<img src="/images/icon-twitter.svg" alt="Twitter" />
		</a>
		<a href="http://pinterest.com" target="_blank" rel="noopener noreferrer">
			<img src="/images/icon-pinterest.svg" alt="Pinterest" />
		</a>
		<a href="http://instagram.com" target="_blank" rel="noopener noreferrer">
			<img src="/images/icon-instagram.svg" alt="Instagram" />
		</a>
	</div>

	<div class="links">
		<a href="# ">About Us</a>
		<a href="# ">Contact</a>
		<a href="# ">Blog</a>
		<a href="# ">Careers</a>
		<a href="# ">Support</a>
		<a href="# ">Privacy Policy</a>
	</div>

	<div class="btnContainer">
		<CustomButton>Request Invite</CustomButton>
	</div>

	<small class="copyright">© Easybank. All Rights Reserved</small>
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
	}

	.socials {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 1rem;
	}

	.links > a {
		margin: 1rem 0;
	}

	.copyright {
		color: var(--clr-text-light);
		font-size: 0.75rem;
	}
</style>
