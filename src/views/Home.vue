<template>
	<div class="home">
		<hero-section />
		<div class="container main-content mt-4">
			<div class="row justify-content-center">
				<div class="col col-11 col-md-4">
					<volunteer-card />
				</div>
				<div class="col video-card col-11 col-md-8 mt-4 mt-md-0">
					<video-card />
				</div>
			</div>
			<div class="row">
				<info-section />
			</div>
		</div>
	</div>
</template>

<script>
// @ is an alias to /src
import HeroSection from "@/components/HeroSection";
import VolunteerCard from "@/components/VolunteerCard";
import VideoCard from "@/components/VideoCard";
import InfoSection from "@/components/InfoSection";
export default {
	name: "home",
	components: {
		HeroSection,
		VolunteerCard,
		VideoCard,
		InfoSection
	}
};
</script>

<style lang="scss">
</style>




