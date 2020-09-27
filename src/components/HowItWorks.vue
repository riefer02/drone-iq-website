<template>
	<div id="about-us">
		<RowHeader title="Drone IQ" />
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
				title: "ABOUT",
				description:
					"Drone IQ is a North-Texas based, early-stage platform company. We are developing the only open software technology platform that manages and secures end-to-end missions of unmanned aircraft systems (UAS) creating a new commercial UAS marketplace.",
			},
			{
				title: "SOFTWARE",
				description:
					"Our unique software technology is an enterprise-class platform that reliably enables and integrates transactions and allows operators and customers to monitor the UAS in real-time when it is beyond visual line of sight (BVLOS).",
			},
			{
				title: "PLATFORMS",
				description:
					"Our cloud-based platform is an ecosystem and an interface that will create a new UAS marketplace that connects drone operators with consumers, providing transaction interaction, integration, and automation. \n Our drone-based EDGE platform will be used on the drone to enable and monitor Beyond Visual Line-of-Sight (BVLOS), to enable inflight management, to automate mission execution, and to perform high-precision location management. ",
			},
		],
	}),
};
</script>

<style>
.min-height {
	min-height: 400px;
}
</style>
