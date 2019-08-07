<template>
	<div class="card pb-0" id="video-card">
		<div class="card-body">
			<h5 class="card-title text-left pl-2 mb-0">
				TESTIMONIAL OF THE MONTH
			</h5>
			<youtube class="video" :video-id="videoId"></youtube>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			videoId: "7Zxm2wcgeYI"
		};
	}
};
</script>

<style lang="scss">
.video iframe {
	width: 100%;
}
.card {
	border: none;
	-webkit-box-shadow: 0px 3px 5px 0px rgba(133, 133, 133, 0.85);
	-moz-box-shadow: 0px 3px 5px 0px rgba(133, 133, 133, 0.85);
	box-shadow: 0px 3px 5px 0px rgba(133, 133, 133, 0.85);
}
.card-body {
	padding: 0;

	.card-title {
		height: 40px;
		line-height: 40px;
		font-family: $font-family-primary;
		font-size: 1rem;
		font-weight: bold;
		color: white;
		background-color: $color-red;
	}
	.card-text {
		font-size: 0.8rem;
	}
}
.card-img {
	border-radius: 0;
	width: 100%;
	object-fit: cover;
}
.btn-join {
	border: 2px solid $color-blue;
	border-radius: 0;
	line-height: 0.8rem;

	a {
		color: $color-blue;
		font-weight: bold;
		font-size: 0.8rem;
	}
}
</style>
