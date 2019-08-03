<template>
	<div id="app">
		<nav-bar />
		<router-view />
	</div>
</template>

<script>
// @ is an alias to /src
import "bootstrap";
import "bootstrap/dist/css/bootstrap.min.css";
import NavBar from "@/components/NavBar.vue";
export default {
	name: "home",
	components: {
		NavBar
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
</style>
