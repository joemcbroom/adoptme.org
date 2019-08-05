<template>
	<div class="sign-up">
		<!-- Button trigger modal -->
		<button
			type="button"
			class="btn btn-outline-secondary"
			data-toggle="modal"
			data-target="#signUpModal"
		>
			Sign Up
		</button>

		<!-- Modal -->
		<div
			class="modal fade"
			id="signUpModal"
			tabindex="-1"
			role="dialog"
			aria-labelledby="signUpModalLabel"
			aria-hidden="true"
		>
			<div class="modal-dialog" role="document">
				<div class="modal-content">
					<div class="modal-header">
						<h5 class="modal-title" id="signUpModalLabel">
							Sign Up To Volunteer
						</h5>
						<button
							type="button"
							class="close"
							data-dismiss="modal"
							aria-label="Close"
						>
							<span aria-hidden="true">&times;</span>
						</button>
					</div>
					<div class="modal-body">
						<div class="form text-left">
							<div class="form-group">
								<label for="name">Name</label>
								<input
									type="text"
									class="form-control"
									id="name"
									placeholder="John Doe"
									v-model="volunteer.name"
								/>
							</div>
							<div class="form-group">
								<label for="quote"
									>Favorite Quote</label
								>
								<textarea
									class="form-control"
									id="quote"
									placeholder="Happiness is not something ready-made. It comes from your own actions."
									v-model="volunteer.favoriteQuote"
								/>
							</div>
							<div class="form-group">
								<label for="color"
									>Favorite Color</label
								>
								<select
									class="form-control"
									id="color"
									v-model="volunteer.favoriteColor"
								>
									<option
										v-for="color in colors"
										:key="color"
										>{{ color }}</option
									>
								</select>
							</div>
							<div class="modal-footer">
								<button
									:disabled="!isValidForm"
									@click="axiosCreateVolunteer"
									data-dismiss="modal"
								>
									Submit
								</button>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import axios from "axios";

export default {
	props: {
		apiURL: String
	},
	data() {
		return {
			volunteer: {
				name: "",
				favoriteQuote: "",
				favoriteColor: ""
			},
			colors: [
				"Red",
				"Orange",
				"Yellow",
				"Green",
				"Blue",
				"Indigo",
				"Violet",
				"Black",
				"Grey",
				"Cornflowerblue"
			]
		};
	},
	methods: {
		createVolunteer() {
			fetch(this.apiURL, {
				method: "POST",
				headers: {
					"Content-Type": "application/json"
				},
				body: JSON.stringify(this.volunteer)
			})
				.then(response => {
					if (response) {
						this.$emit("showVolunteers");
					}
				})
				.catch(err => console.error(err));
		},
		axiosCreateVolunteer() {
			axios.post(this.apiURL, this.volunteer)
				.then(response => {
					if (response) {
						this.$emit("axiosShowVolunteers");
					}
				})
				.catch(err => console.error(err));
		}
	},
	computed: {
		isValidForm() {
			return (
				this.volunteer.name != "" &&
				this.volunteer.favoriteQuote != ""
			);
		}
	}
};
</script>

<style lang="scss" scoped>
</style>
