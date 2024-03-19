<section aria-labelledby="hArticles" class="articles">
	<h2 id="hArticles">Latest Articles</h2>

	<div class="articleContainer">
		<div class="article">
			<img src="/images/image-currency.jpg" alt="Currency" />
			<div class="content">
				<small class="author">By Claire Robinson</small>
				<h3>Receive money in any currency with no fees</h3>
				<small
					>The world is getting smaller and we’re becoming more mobile. So why should you be forced
					to only receive money in a single …</small
				>
			</div>
		</div>

		<div class="article">
			<img src="/images/image-restaurant.jpg" alt="Restaurant" />
			<div class="content">
				<small class="author">By Wilson Hutton</small>
				<h3>Treat yourself without worrying about money</h3>
				<small
					>Our simple budgeting feature allows you to separate out your spending and set realistic
					limits each month. That means you …</small
				>
			</div>
		</div>

		<div class="article">
			<img src="/images/image-plane.jpg" alt="Plane" />
			<div class="content">
				<small class="author">By Wilson Hutton</small>
				<h3>Take your Easybank card wherever you go</h3>
				<small
					>We want you to enjoy your travels. This is why we don’t charge any fees on purchases
					while you’re abroad. We’ll even show you …</small
				>
			</div>
		</div>

		<div class="article">
			<img src="/images/image-confetti.jpg" alt="Confetti" />
			<div class="content">
				<small class="author">By Claire Robinson</small>
				<h3>Our invite-only Beta accounts are now live!</h3>
				<small
					>After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s
					easy to request an invite through the site …</small
				>
			</div>
		</div>
	</div>
</section>

<style>
	.articles {
		padding: 2rem 0;
	}

	h2 {
		display: block;
		max-width: 35ch;
		margin: 1rem auto;
		text-align: center;
	}

	h2 {
		font-size: 2rem;
		font-weight: var(--fw-light);
	}

	.article {
		font-size: 1rem;
		margin: 2rem 1rem;
		border-radius: 1rem;
		background-color: var(--clr-base);
		overflow: hidden;
	}

	.article img {
		width: 100%;
		aspect-ratio: 1.618;
		object-fit: cover;
	}

	.article .content {
		padding: 1.5rem 1rem;
	}

	.article h3 {
		font-weight: var(--fw-normal);
		font-size: 1.1em;
		margin: 0.75rem auto;
	}

	.article .author {
		color: var(--clr-text-light);
		font-size: 0.7em;
	}

	.article small {
		color: var(--clr-text-light);
		display: block;
		font-size: 0.8em;
	}

	@media (width >= 800px) {
		.articles {
			padding: 3rem 10%;
		}

		h2 {
			text-align: left;
			margin-inline: 0;
			margin-bottom: 2rem;
		}

		.articleContainer {
			display: flex;
			gap: 1rem;
		}

		.article {
			flex: 1;
			margin: 0;
			font-size: 0.8rem;
			border-radius: 0.5rem;
		}

		.article > img {
			aspect-ratio: 0;
			max-height: 8rem;
		}
	}
</style>
