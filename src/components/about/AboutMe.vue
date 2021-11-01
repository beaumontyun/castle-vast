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
          bio: "Castle Vast specialise in private investments, private wealth and assets, and long term investment holdings.",
        },
        {
          id: 2,
          bio: "We take aim at a balanced portfolio with a stable and sustainable investment strategy but adopt a minimum level of investment risks to secure a healthy growth to our portfolio against the changes of time. Just like our namesake, we maintain the walls and pillars of the castle without neglecting to capture the vast lands and opportunities that surround us.",
        },
        {
          id: 3,
          bio: "At Castle Vast, we pride ourselves in having a deep knowledge and technical know-how on our investments. All members of our firm have specialised knowledge in the law, finance, computer programming, engineering, political science, and many others. It is our core belief that one must have the necessary sensitivity to the technical aspect of a trade in order to assess investment risks, to put our beneficiaries as priority above all else.",
        },
        {
          id: 4,
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
