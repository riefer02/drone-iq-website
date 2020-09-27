<template>
	<div id="partners">
		<RowHeader title="Partners" />
		<v-row class="d-flex justify-center">
			<PartnerLogo v-for="item in items" :key="item.title" :item="item" />
		</v-row>
	</div>
</template>

<script>
import PartnerLogo from "@/components/PartnerLogo.vue";
import RowHeader from "@/components/RowHeader.vue";
export default {
	name: "Partners",
	components: {
		PartnerLogo,
		RowHeader,
	},
	data: () => ({
		items: [
			{
				title: "BNSF Railway",
				image: "bnsf-logo.png",
			},
			{
				title: "Microsoft",
				image: "microsoft-logo.png",
			},
			{
				title: "Bell",
				image: "bell-logo.png",
			},
			{
				title: "University of North Texas",
				image: "unt-logo.png",
			},
			{
				title: "Life Gift",
				image: "life-gift-logo.png",
			},
		],
	}),
};
</script>
