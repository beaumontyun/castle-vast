<template>
	<div class="container mx-auto">
		<!-- Banner start -->
		<Banner />
		<!-- Banner snd -->

		<!-- Projects start -->
		<AboutMe />
		<!-- Projects end -->


	</div>
</template>

<script>
import Banner from '@/components/home/Banner';
import AboutMe from '@/components/about/AboutMe';
import feather from 'feather-icons';

export default {
	name: 'Home',
	components: {
		Banner,
		AboutMe,
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
