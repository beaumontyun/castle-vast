<template>
	<div class="container mx-auto ">
		<div
			class="innercontent pt-20 sm:pt-30 pb-8 mt-20 border-t-2 border-primary-light dark:border-secondary-dark"
		>
			<!-- Footer social links start -->
			<div
				class="flex flex-col justify-center items-center mb-12 sm:mb-28"
			>
				<p
					class="text-3xl sm:text-4xl font-medium text-blue-900 dark:text-primary-light mb-5"
				>
					Contact us
				</p>
				<ul class="flex gap-4 sm:gap-8">
					<p class="mb-4 text-ternary-dark dark:text-ternary-light text-lg">+852 6279 6046</p>
					<a class="mb-4 text-ternary-dark dark:text-ternary-light text-lg">corporate@castle-vast.com</a>
				</ul>
			</div>
			<!-- Footer social links end -->

			<!-- Footer copyright start -->
			<div class="flex justify-center items-center text-center">
				<div class="text-sm text-ternary-dark dark:text-ternary-light">
					&copy; Copyright {{ copyrightDate }}. Castle Vast Limited, Hong Kong SAR.
				</div>
			</div>
			<!-- Footer copyright end -->
		</div>
	</div>
</template>

<script>
import feather from 'feather-icons';
export default {
	data() {
		return {
			copyrightDate: new Date().getFullYear(),
		};
	},
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
};
</script>

<style scoped></style>
