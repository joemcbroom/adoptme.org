/* eslint-disable */
<template>
	<div class="img-container container-fluid">
		<div class="row justify-content-center img-text">
			<div class="col col-md-10 text-left">
				<h2>This is your new family!</h2>
				<router-link
					:to="{ name: 'home' }"
					class="btn btn-outline-danger"
					tag="button"
					>ADOPT NOW</router-link
				>
			</div>
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.container-fluid {
	padding: 0;
}

.img-container {
	display: flex;
	align-items: flex-end;
	height: 40vh;
	width: 100%;
	background: url("../assets/img/dogs.jpg");
	// background-attachment: fixed;
	background-repeat: no-repeat;
	background-size: cover;
	background-position: center;

	.img-text {
		width: 100%;
		background-color: rgba(0, 0, 0, 0.4);
		padding-top: 10px;
		padding-bottom: 10px;
		margin: 0;

		h2 {
			color: $color-red;
			font-family: $font-family-secondary;
		}
		.btn {
			border-radius: 0;
			border: 2px solid $color-red;
			line-height: 1rem;
		}
		.btn:hover {
			background-color: transparent;
		}
		.btn {
			font-family: $font-family-primary;
			color: $color-red;
			font-weight: bold;
			font-size: 0.8rem;
		}
		.btn-outline-danger:hover {
			text-shadow: 1px 1px 1px black;
			text-decoration: none;
		}
	}
}
@media only screen and (max-width: 768px) {
	.img-container {
		height: 30vh;
		background-position: center;
	}
}
</style>
