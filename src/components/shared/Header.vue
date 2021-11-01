<template>
	<nav id="nav" class="sm:container sm:mx-auto">
		<!-- Header start -->
		<div
			class="z-10 max-w-screen-lg xl:max-w-screen-xl block sm:flex sm:justify-between sm:items-center my-6"
		>
			<!-- Header menu links and small screen humberger menu start -->
			<div class="flex justify-between items-center px-4 sm:px-0">
				<!-- Header logos start -->
				<div>
					<router-link to="/"
						><img
							v-if="theme === 'light'"
							src="../../assets/images/logo-dark.svg"
							class="w-48"
							alt="Blue Logo"
						/>
						<img
							v-else
							src="../../assets/images/logo-light.svg"
							class="w-48"
							alt="White Logo"
						/>
					</router-link>
				</div>
				<!-- Header logos end -->

				<!-- Theme switcher small screen start -->
				<theme-switcher
					:theme="theme"
					@themeChanged="updateTheme"
					class="block sm:hidden bg-ternary-light dark:bg-ternary-dark hover:bg-hover-light dark:hover:bg-hover-dark hover:shadow-sm px-2.5 py-2 rounded-lg ml-10"
				/>
				<!-- Theme switcher small screen end -->

			</div>
			<!-- Header menu links and small screen humberger menu end -->

			<!-- Header links start -->
			<div
				:class="isOpen ? 'block' : 'hidden'"
				class="m-0 sm:ml-4 mt-5 sm:mt-3 sm:flex p-5 sm:p-0 justify-center items-center shadow-lg sm:shadow-none"
			>
			</div>
			<!-- Header links end -->

			<!-- Header right section buttons start -->
			<div
				class="hidden sm:flex justify-between items-center flex-col md:flex-row"
			>

				<!-- Theme switcher largr screen start -->
				<theme-switcher
					:theme="theme"
					@themeChanged="updateTheme"
					class="ml-8 bg-primary-light dark:bg-ternary-dark px-3 py-2 shadow-sm rounded-xl cursor-pointer"
				/>
				<!-- Theme switcher largr screen end -->
			</div>
			<!-- Header right section buttons stendart -->
		</div>
		<!-- Header end -->
	</nav>
</template>

<script>
import ThemeSwitcher from '../ThemeSwitcher';
import feather from 'feather-icons';

export default {
	components: {
		ThemeSwitcher,
	},
	data() {
		return {
			theme: '',
			modal: false,
		};
	},

	created() {
		this.theme = localStorage.getItem('theme') || 'light';
	},
	mounted() {
		feather.replace();
		this.theme = localStorage.getItem('theme') || 'light';
	},
	methods: {
		updateTheme(theme) {
			this.theme = theme;
		},
		showModal() {
			if (this.modal) {
				// Stop screen scrolling
				document
					.getElementsByTagName('html')[0]
					.classList.remove('overflow-y-hidden');
				this.modal = false;
			} else {
				document
					.getElementsByTagName('html')[0]
					.classList.add('overflow-y-hidden');
				this.modal = true;
			}
		},
	},
	updated() {
		feather.replace();
	},
};
</script>

<style scoped>
#nav a.router-link-exact-active {
	@apply text-indigo-700;
	@apply dark:text-indigo-400;
	@apply font-medium;
}

.modal-body {
	max-height: 500px;
}
.bg-gray-800-opacity {
	background-color: #2d374850;
}
@media screen and (max-width: 768px) {
	.modal-body {
		max-height: 400px;
	}
}
.fade-up-down-enter-active {
	transition: all 0.3s ease;
}
.fade-up-down-leave-active {
	transition: all 0.3s ease;
}
.fade-up-down-enter {
	transform: translateY(10%);
	opacity: 0;
}
.fade-up-down-leave-to {
	transform: translateY(10%);
	opacity: 0;
}

.fade-enter-active {
	-webkit-transition: opacity 2s;
	transition: opacity 0.3s;
}
.fade-leave-active {
	transition: opacity 0.3s;
}

.fade-enter,
.fade-leave-to {
	opacity: 0;
}
</style>
