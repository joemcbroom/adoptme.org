<template>
	<div id="app">
		<nav-bar />
		<router-view />
		<footer-nav />
	</div>
</template>

<script>
// @ is an alias to /src
import "bootstrap";
import "bootstrap/dist/css/bootstrap.min.css";
import NavBar from "@/components/NavBar.vue";
import FooterNav from "@/components/FooterNav";

export default {
	name: "home",
	components: {
		NavBar,
		FooterNav
	}
};
</script>

<style lang="scss">
#app {
	font-family: $font-family-primary;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
}
h1 {
	color: $color-blue;
	font-size: $font-size-h1;
}
.btn {
	width: 112px !important;
}
.btn-outline-danger {
	border-radius: 0;
	border: 2px solid $color-red;
	line-height: 1rem;
	font-family: $font-family-primary;
	color: $color-red;
	font-weight: bold;
	font-size: 0.8rem;
}
</style>
