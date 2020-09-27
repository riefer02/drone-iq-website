<template>
	<div>
		<RowHeader title="Who We Are" />
		<v-row class="d-flex justify-center">
			<Card v-for="item in items" :key="item.title" :item="item" />
		</v-row>
	</div>
</template>

<script>
import Card from "@/components/Card.vue";
import RowHeader from "@/components/RowHeader.vue";

export default {
	components: {
		Card,
		RowHeader,
	},
	data: () => ({
		items: [
			{
				title: "OUR MISSION",
				description:
					"To deliver the technology and processes that enable, integrate, and secure transactions in a new commercial marketplace for unmanned aircraft systems",
				icon: "earth",
			},
			{
				title: "OUR VISION",
				description:
					"Integrated and secured transactions for unmanned aircraft ecosystems.",
				icon: "telescope",
			},
			{
				title: "OUR VALUES",
				description:
					"Innovation, Integration, Integrity, & Collaboration",
				icon: "hand-heart-outline",
			},
			{
				title: "OUR GOAL",
				description:
					'Our goal is to be the "Uber" or "Lyft" platform that creates a new UAS commercial marketplace',
				icon: "star",
			},
		],
	}),
};
</script>

<style></style>
