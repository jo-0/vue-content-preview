<template>
	<div class="container">
		<div class="card-container">
			<card
				v-for="user in users"
				:key="user.id"
				:user-name="user.name"
				:website="user.website"
				@click.native="showPreview(user)"
			/>
		</div>
		<preview />
	</div>
</template>

<script>
import Card from "@/components/card";
import Users from "@/users";
import Preview from "@/components/preview";

export default {
	name: "App",
	components: {
		Card,
		Preview
	},
	data() {
		return {
			users: Users.users,
			isPreviewActive: false
		};
	},
	methods: {
		showPreview(user) {
			console.log(user.name);
		}
	}
};
</script>

<style lang="scss" scoped>
.container {
	display: flex;
	margin: 20px 60px;
}

.card-container {
	display: flex;
	flex-wrap: wrap;
	margin: 20px 60px;
}
</style>
