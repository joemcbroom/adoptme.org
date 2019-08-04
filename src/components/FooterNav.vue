<template>
	<div class="container-fluid">
		<div class="row footer">
			<div class="col col-11 col-md-3 footer-left text-md-left">
				<router-link
					class="footer-home-link"
					:to="{ name: 'home' }"
				>
					<img
						class="logo py-3 pr-2"
						src="@/assets/img/logo.png"
					/>Adoptme.Org</router-link
				>
				<p class="mb-0">Main St #1245</p>
				<p>Amazing City, 45677</p>
				<p class="disclaimer">
					Some images were taken from unsplash.com
				</p>
			</div>
			<div
				class="col col-11 col-md-7 footer-right d-flex justify-content-start align-items-center"
			>
				<ul class="list-inline">
					<li class="list-inline-item">
						<a href="#">WHAT we do</a>
					</li>
					<li class="list-inline-item">
						<a href="#">WHO we are</a>
					</li>
					<li class="list-inline-item">
						<a href="#">EVENTS adoption</a>
					</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.footer {
	background-color: $color-blue;
	min-height: 30vh;
	border-top: 4px solid $color-red;

	.footer-home-link {
		color: white;
		font-family: $font-family-secondary;
		font-size: 2.5rem;

		img {
			height: 75px;
		}
	}

	.footer-left {
		margin: 5% 0 5% 8%;

		p {
			color: white;
			font-size: 0.9rem;
		}
		.disclaimer {
			font-size: 0.4rem;
			padding-top: 10%;
		}
	}

	.footer-right {
		padding-left: 5%;

		ul {
			width: 100%;
			text-align: left;
		}
		li {
			padding-right: 2%;
		}
		a {
			color: white;
			font-weight: bold;
		}
	}
}
@media only screen and (max-width: 768px) {
	.footer {
		justify-content: center;

		.footer-left {
			margin: 0;
			display: flex;
			flex-direction: column;
			justify-content: center;

			.disclaimer {
				padding: 0;
			}
		}

		p {
			text-align: center;
		}
		.footer-right {
			justify-content: center;

			ul {
				text-align: center;
			}
		}
	}
}
</style>
