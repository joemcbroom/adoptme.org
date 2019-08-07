<template>
	<div class="volunteers container-fluid pt-4">
		<h2 class="h2-volunteers">Meet Our Volunteers</h2>
		<sign-up
			:apiURL="apiURL"
			@axiosShowVolunteers="axiosShowVolunteers()"
		/>
		<div class="row justify-content-center align-items-stretch">
			<div
				v-for="volunteer in volunteers.slice().reverse()"
				:key="volunteer.id"
				class="col col-auto m-4"
			>
				<div class="card">
					<h5
						class="card-title text-center pl-2 mb-0"
						:style="{
							backgroundColor: volunteer.favoriteColor.replace(
								/\s+/g,
								''
							)
						}"
					>
						<span class="title-span px-1">
							{{ volunteer.name }}
						</span>
					</h5>
					<div class="card-body p-2">
						<p>
							<img
								class="avatar mt-2"
								:src="volunteer.avatar"
							/>
						</p>
						<p class="quote">
							Favorite Quote:
							<em>"{{ volunteer.favoriteQuote }}"</em>
						</p>
						<p class="color">
							Favorite Color:
							<em>"{{ volunteer.favoriteColor }}"</em>
						</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import axios from "axios";
import SignUp from "@/components/SignUp";

export default {
	name: "volunteers",
	components: {
		SignUp
	},

	data() {
		return {
			apiURL:
				"http://5d4732e1992ea9001444c7f9.mockapi.io/api/volunteers",
			volunteers: []
		};
	},
	methods: {
		showVolunteers() {
			fetch(this.apiURL)
				.then(response => {
					return response.json();
				})
				.then(volunteers => {
					this.volunteers = volunteers;
				})
				.catch(err => console.error(err));
		},
		axiosShowVolunteers() {
			axios.get(this.apiURL)
				.then(response => {
					this.volunteers = response.data;
					console.log(this.volunteers);
				})
				.catch(err => console.error(err));
		}
	},
	created() {
		this.axiosShowVolunteers();
	}
};
</script>

<style lang="scss" scoped>
.h2-volunteers {
	font-family: $font-family-secondary;
}
.card {
	width: 18rem;
	height: 100%;
}
.card-title {
	color: white;
	line-height: 3rem;

	span {
		background-color: white;
		color: black;
		border: 1px solid black;
	}
}
.avatar {
	border: 2px solid black;
	border-radius: 50%;
}
.quote,
.color {
	text-transform: capitalize;
}
</style>
