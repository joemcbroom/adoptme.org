<template>
	<div class="behavior-program">
		<div class="row mb-3">
			<div class="col col-3 d-flex align-items-center">
				<img
					class="info-section-img"
					src="@/assets/img/friend-in-trouble.png"
				/>
			</div>
			<div
				class="col col-9 text-left d-flex flex-column justify-content-center"
			>
				<h6 class="info-section-header">BEHAVIOR PROGRAM</h6>
				<p>
					Evaluation of each dog using specialists who determine
					the best training that will help your friend be a
					better family member
				</p>
				<button class="btn btn-outline-danger">Read More</button>
			</div>
		</div>

		<div class="row">
			<div class="col col-3 d-flex align-items-center">
				<img
					class="info-section-img"
					src="@/assets/img/fluffydog.jpg"
				/>
			</div>
			<div
				class="col col-9 text-left d-flex flex-column justify-content-center"
			>
				<h6 class="info-section-header">MY NEXT FAMILY</h6>
				<p>
					Are you looking for a new family member? Then, this
					program is for you. Don't buy, adopt here, and let's
					give a home to these amazing friends
				</p>
				<button class="btn btn-outline-danger">Read More</button>
			</div>
		</div>
	</div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.info-section-header {
	color: $color-red;
	font-family: $font-family-primary;
	font-weight: bold;
}
.info-section-img {
	width: 100%;
	margin: auto;
}
.btn {
	width: 100px;
}
</style>
