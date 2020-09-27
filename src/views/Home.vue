<template>
	<div class="home">
		<Header />
		<v-container>
			<div class="min-row-height">
				<HowItWorks />
			</div>
			<v-divider />
			<div class="min-row-height">
				<AboutUs />
			</div>
			<v-divider />
			<div class="min-row-height mb-10">
				<Team />
			</div>
			<v-divider />
			<div class="min-row-height">
				<Partners />
			</div>
			<v-divider />
			<div class="min-row-height">
				<Contact />
			</div>
		</v-container>
	</div>
</template>

<script>
// @ is an alias to /src
import Header from "@/components/Header.vue";
import HowItWorks from "@/components/HowItWorks.vue";
import AboutUs from "@/components/AboutUs.vue";
import Team from "@/components/Team.vue";
import Partners from "@/components/Partners.vue";
import Contact from "@/components/Contact.vue";

export default {
	name: "Home",
	components: { Header, HowItWorks, AboutUs, Team, Partners, Contact },
};
</script>

<style>
.min-row-height {
	min-height: 400px;
}
</style>
