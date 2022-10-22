<template>
	<div class="container mx-auto">
		<!-- Banner start -->
		<Banner />
		<!-- Banner snd -->

		<!-- AboutMe start -->
		<AboutMe />
		<!-- AboutMe end -->

		<!-- Project start -->
		<!-- <Projects /> -->
		<!-- Project ends -->

	</div>
</template>

<script>
import Banner from '@/components/home/Banner';
import AboutMe from '@/components/about/AboutMe';
// import Projects from "@/components/about/Projects"
import feather from 'feather-icons';

export default {
	name: 'Home',
	components: {
		Banner,
		AboutMe,
		// Projects
	},
	data: () => {
		return {};
	},
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
	methods: {},
};
</script>

<style scoped></style>
