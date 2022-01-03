<template>
  <!-- <div
    class="block sm:gap-10 mt-10 text-left sm:flex"
  > -->
    <!-- <div class="w-full sm:w-1/4 mb-7 sm:mb-0"></div> -->
    <div class="w-full">
      <p
        v-for="bio in bios"
        :key="bio.id"
        class="mb-4 text-ternary-dark dark:text-ternary-light text-lg"
      >
        {{ bio.bio }}
      </p>
      <a
        href="http://www.mysitio.co.uk"
        class="text-ternary-dark dark:text-ternary-light"
        >http://www.mysitio.co.uk</a
      >
    </div>
  <!-- </div> -->
</template>

<script>
export default {
  props: ["modal"],
  setup() {
    return {
      bios: [
        {
          id: 1,
          bio: "Sitio is a project developed for catering the market gap on home decor and interior design section.",
        },
        {
          id: 2,
          bio: "It is a platform to match home owners with service providers for decoration and interior design service.",
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
