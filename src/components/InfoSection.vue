<template>
	<div class="container mt-3">
		<div class="row justify-content-start">
			<div class="col col-11 col-md-8">
				<ul class="nav" id="info-tabs" role="tablist">
					<li class="nav-item text-left mr-4">
						<a
							class="nav-link active pl-0 pr-1 pb-1"
							id="programs-tab"
							data-toggle="tab"
							href="#programs"
							role="tab"
							aria-controls="home"
							aria-selected="true"
							>PROGRAMS</a
						>
					</li>
					<li class="nav-item text-left">
						<a
							class="nav-link pl-0 pr-1 pb-1"
							id="companies-tab"
							data-toggle="tab"
							href="#companies"
							role="tab"
							aria-controls="home"
							aria-selected="true"
							>ASSOCIATED COMPANIES</a
						>
					</li>
				</ul>
				<div
					class="tab-content d-flex justify-content-start align-items-center p-3"
				>
					<div
						class="tab-pane active"
						id="programs"
						role="tabpanel"
						aria-labelledby="programs-tab"
					>
						<behavior-program />
					</div>
					<div
						class="tab-pane"
						id="companies"
						role="tabpanel"
						aria-labelledby="companies-tab"
					>
						<associated-companies />
					</div>
				</div>
			</div>
			<div class="col col-11 col-md-4 d-flex align-items-center">
				<img
					class="dog-img"
					src="@/assets/img/cutedog.png"
					alt="Cute Dog"
				/>
			</div>
		</div>
	</div>
</template>

<script>
import BehaviorProgram from "@/components/BehaviorProgram";
import AssociatedCompanies from "@/components/AssociatedCompanies";

export default {
	components: {
		BehaviorProgram,
		AssociatedCompanies
	}
};
</script>

<style lang="scss">
.nav-item a {
	color: $color-blue;
	font-weight: bold;
}
.nav-link.active {
	border-bottom: 3px solid $color-blue;
}
.dog-img {
	width: 40%;
	margin: auto;
}
@media only screen and (max-width: 768px) {
	.dog-img {
		width: 20%;
	}
}
</style>
