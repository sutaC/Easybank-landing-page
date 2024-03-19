<section class="information" aria-labelledby="hInformation">
	<div class="header">
		<h2 id="hInformation">Why choose Easybank?</h2>
		<small>
			We leverage Open Banking to turn your bank account into your financial hub. Control your
			finances like never before.
		</small>
	</div>

	<div class="points">
		<div class="point">
			<img src="/images/icon-online.svg" alt="Online" />
			<h3>Online Banking</h3>
			<small
				>Our modern web and mobile applications allow you to keep track of your finances wherever
				you are in the world.</small
			>
		</div>

		<div class="point">
			<img src="/images/icon-budgeting.svg" alt="Budgeting" />
			<h3>Simple Budgeting</h3>
			<small
				>See exactly where your money goes each month. Receive notifications when you’re close to
				hitting your limits.</small
			>
		</div>

		<div class="point">
			<img src="/images/icon-onboarding.svg" alt="Onboarding" />
			<h3>Fast Onboarding</h3>
			<small
				>We don’t do branches. Open your account in minutes online and start taking control of your
				finances right away.</small
			>
		</div>

		<div class="point">
			<img src="/images/icon-api.svg" alt="Api" />
			<h3>Open API</h3>
			<small>
				Manage your savings, investments, pension, and much more from one account. Tracking your
				money has never been easier.</small
			>
		</div>
	</div>
</section>

<style>
	.information {
		padding: 2rem 0;
		background-color: var(--clr-section-bg);
		z-index: -1;
	}

	.point {
		text-align: center;
		margin: 2.5rem auto;
	}

	h2,
	h3,
	small {
		display: block;
		max-width: 35ch;
		margin: 1rem auto;
		text-align: center;
	}

	h2 {
		font-size: 2rem;
		font-weight: var(--fw-light);
	}

	h3 {
		font-size: 1.25rem;
		font-weight: var(--fw-light);
	}

	small {
		color: var(--clr-text-light);
	}

	@media (width >= 800px) {
		.information {
			position: relative;
			z-index: -1;
			padding-inline: 10%;
		}

		.header {
			text-align: left;
		}

		.points {
			display: flex;
			gap: 2rem;
			align-items: baseline;
		}

		.point {
			flex: 1;
			text-align: left;
		}

		h2,
		h3,
		small {
			text-align: left;
			margin-inline: 0;
			max-width: 50ch;
		}
	}
</style>
