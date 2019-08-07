<template>
	<div class="nav-bar">
		<nav class="navbar navbar-expand-md  py-md-2 px-md-4 px-1">
			<router-link class="navbar-brand mr-auto" :to="{ name: 'home' }">
				<img
					class="logo"
					src="@/assets/img/logo.png"
				/>Adoptme.Org</router-link
			>
			<button
				class="navbar-toggler"
				type="button"
				data-toggle="collapse"
				data-target="#navbarTop"
				aria-controls="navbarTop"
				aria-expanded="false"
				aria-label="Toggle navigation"
			>
				<span class="navbar-toggler-icon"
					><font-awesome-icon icon="bars"
				/></span>
			</button>

			<div
				class="collapse navbar-collapse navbar-right"
				id="navbarTop"
			>
				<ul class="navbar-nav ml-auto">
					<li class="nav-item">
						<a class="nav-link" href="#">WHAT we do</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" href="#">WHO we are</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" href="#">EVENTS adoption</a>
					</li>
				</ul>
			</div>
		</nav>
	</div>
</template>

<script>
export default {
	data() {
		return {
			logoURL: "@/assets/img/logo.png"
		};
	}
};
</script>



<style lang="scss">
.navbar {
	background-color: $color-red;

	a {
		color: white;
	}
	a.nav-link:hover {
		cursor: pointer;
	}
	li > a {
		color: white;
	}
	.navbar-brand {
		font-family: $font-family-secondary;
		font-size: 2.5rem;
	}
	.navbar-right {
		font-weight: bold;
		font-size: 1rem;
	}
	.logo {
		height: 50px;
		padding-right: 5px;
	}
	.nav-item {
		margin-left: 10px;
		white-space: nowrap;
	}
}
.navbar-toggler {
	color: white;
	border: 1px solid white;

	svg {
		height: 100%;
		margin: auto;
	}
}
</style>
