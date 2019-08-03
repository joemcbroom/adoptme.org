<template>
	<div class="home">
		<hero-section />
		<div class="container main-content mt-4">
			<div class="row justify-content-center align-items-center">
				<div class="col justify-content-center col-11 col-sm-4">
					<volunteer-card />
				</div>
				<div class="col video-card col-11 col-sm-8 mt-4 mt-sm-0">
					<video-card />
				</div>
			</div>
		</div>
	</div>
</template>

<script>
// @ is an alias to /src
import HeroSection from "@/components/HeroSection";
import VolunteerCard from "@/components/VolunteerCard";
import VideoCard from "@/components/VideoCard";
export default {
	name: "home",
	components: {
		HeroSection,
		VolunteerCard,
		VideoCard
	}
};
</script>

<style lang="scss">
.video-card {
	max-height: 335px;
}
</style>




