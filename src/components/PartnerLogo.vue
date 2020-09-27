<template>
	<div class="d-flex justify-center">
		<v-img
			:src="require('@/assets/images/' + item.image)"
			max-width="300"
			class="align-self-center mx-4"
		></v-img>
	</div>
</template>

<script>
export default {
	name: "PartnerLogo",
	props: {
		item: {
			type: Object,
			required: true,
		},
	},
	data: () => ({}),
};
</script>
