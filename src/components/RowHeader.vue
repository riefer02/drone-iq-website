<template>
	<v-row>
		<v-col class="d-flex justify-center mt-10 mb-10">
			<h1>{{ title }}</h1>
		</v-col>
	</v-row>
</template>

<script>
export default {
	props: {
		title: {
			type: String,
			required: true,
		},
	},
	data: () => ({}),
};
</script>
