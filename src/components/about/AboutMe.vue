<template>
  <div class="block sm:flex sm:gap-10 mt-10 sm:mt-20">
    <!-- About me portfolio image start -->
    <div class="w-full sm:w-1/4 mb-7 sm:mb-0">
      <div>
        <div class="text-left dark:text-ternary-light text-ternary-dark text-3xl sm:text-5xl">ABOUT</div>
        <!-- <img
          v-if="theme === 'light'"
          src="../../assets/images/about-logo-dark.svg"
          class="w-24 sm:w-48"
          alt="Blue Logo"
        />
        <img
          v-else
          src="../../assets/images/about-logo-light.svg"
          class="w-24 sm:w-48"
          alt="White Logo"
        /> -->
      </div>
    </div>
    <!-- About me portfolio image end -->

    <!-- About me details start -->
    <div class="w-full sm:w-3/4 text-left">
      <p
        v-for="bio in bios"
        :key="bio.id"
        class="mb-4 text-ternary-dark dark:text-ternary-light sm:text-2xl"
      >
        {{ bio.bio }}
      </p>
    </div>
    <!-- About me details end -->
  </div>
</template>

<script>
export default {
  setup() {
    return {
      bios: [
        {
          id: 1,
          bio: "At Castle Vast, we focus on the next generation technology that helps to improve the lives of our society.",
        },
        {
          id: 2,
          bio: "With our knowledge and technical know-how, we possess the sensitivity and skills to create sustainable projects, placing our stakeholders as priority above all else.",
        },
        {
          id: 3,
          bio: "We look forward to share more of our stories and success to you, please reach out to one of our representatives for our latest offering.",
        },
      ],
    };
  },
  data() {
    return {
      theme: "",
    };
  },
  created() {
    this.theme = localStorage.getItem("theme") || "light";
  },
  mounted() {
    this.theme = localStorage.getItem("theme") || "light";
  },
};
</script>
