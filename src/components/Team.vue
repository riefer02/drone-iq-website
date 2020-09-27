<template>
	<div id="team">
		<RowHeader title="Our Team" />
		<v-row>
			<AvatarCard v-for="item in items" :key="item.title" :item="item" />
		</v-row>
	</div>
</template>

<script>
import AvatarCard from "@/components/AvatarCard.vue";
import RowHeader from "@/components/RowHeader.vue";
export default {
	name: "Team",
	components: {
		AvatarCard,
		RowHeader,
	},
	data: () => ({
		items: [
			{
				name: "David Sanders",
				image: "",
				position: "Interim Chief Executive Officer",
				description:
					"David Sanders is a senior executive with 40 years of experience in innovation and optimization of technology and technology services companies. He has worked with start-up technology companies all the way to large global technology companies, with firms such as Accenture, BearingPoint, SHL Systemhouse, ISG/TPI and Perot Systems.  ",
			},
		],
	}),
};
</script>
