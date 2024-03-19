<script>
	import CustomButton from '$lib/components/CustomButton.svelte';
</script>

<section aria-labelledby="hHero" class="hero">
	<div class="banner">
		<img src="/images/image-mockups.png" alt="Mockups" />
	</div>

	<div class="content">
		<h1 id="hHero">Next generation digital banking</h1>
		<small>
			Take your financial life online. Your Easybank account will be a one-stop-shop for spending,
			saving, budgeting, investing, and much more.
		</small>

		<div class="buttonContainer">
			<CustomButton>Request Invite</CustomButton>
		</div>
	</div>
</section>

<style>
	.hero {
		margin-bottom: 4rem;
	}

	.banner {
		position: relative;
		width: 100%;
		aspect-ratio: 1;
		background-image: url('/images/bg-intro-mobile.svg');
		background-repeat: no-repeat;
		background-size: cover;
		background-position: center;
		z-index: 1;
	}

	.banner > img {
		width: 100%;
		position: absolute;
		top: -30%;
	}

	h1,
	small {
		display: block;
		max-width: 35ch;
		text-align: center;
		font-weight: var(--fw-light);
	}

	h1 {
		margin: 0.5rem auto;
		font-size: 2.25rem;
	}

	small {
		margin: 1rem auto;
		color: var(--clr-text-light);
	}

	.buttonContainer {
		text-align: center;
		margin: 1.5rem auto;
	}

	@media (width >= 800px) {
		.hero {
			display: flex;
			flex-direction: row-reverse;
			margin-bottom: 0;
			max-height: 25rem;
		}

		.banner {
			background-image: url('/images/bg-intro-desktop.svg');
			background-size: 150%;
			background-position: left;
		}

		.banner > img {
			height: 140%;
			width: auto;
			top: -15%;
			right: -10%;
		}

		.content {
			display: flex;
			justify-content: center;
			flex-direction: column;
			gap: 1rem;
			padding-inline: 10%;
		}

		.content > * {
			text-align: left;
			margin: 0;
			width: 100%;
		}
	}
</style>
