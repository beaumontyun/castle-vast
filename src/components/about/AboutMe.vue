<template>
  <div class="block sm:flex sm:gap-10 mt-10 sm:mt-20">
    <!-- About me portfolio image start -->
    <div class="w-full sm:w-1/4 mb-7 sm:mb-0">
      <div>
        <img
          v-if="theme === 'light'"
          src="../../assets/images/about-logo-dark.svg"
          class="w-24 sm:w-96"
          alt="Blue Logo"
        />
        <img
          v-else
          src="../../assets/images/about-logo-light.svg"
          class="w-24 sm:w-96"
          alt="White Logo"
        />
      </div>
    </div>
    <!-- About me portfolio image end -->

    <!-- About me details start -->
    <div class="w-full sm:w-3/4 text-left">
      <p
        v-for="bio in bios"
        :key="bio.id"
        class="mb-4 text-ternary-dark dark:text-ternary-light text-lg"
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
          bio: "At Castle Vast, we are focusing on the next generation technology and social application projects that help improve the lives of our society and to discover the market gap that is left unfilfulled.",
        },
        {
          id: 2,
          bio: "We pride ourselves in having a deep knowledge and technical know-how. All members of our team have specialised knowledge in the law, finance, computer programming, engineering, political science, and many others. It is our core belief that one must have the necessary sensitivity to the technical aspect of a trade in order to create sustainable projects, to put the benefits of our stakeholders as priority above all else.",
        },
        {
          id: 3,
          bio: "We look forward to share more of our stories and success to you. Please reach out to one of our representatives to browse our latest offering.",
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
