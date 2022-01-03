<template>
  <div class="block sm:flex sm:gap-10 mt-10 sm:mt-20">
    <!-- Project image start -->
    <div class="w-full sm:w-1/4 mb-7 sm:mb-0">
      <div>
        <img
          v-if="theme === 'light'"
          src="../../assets/images/projects-logo-dark.svg"
          class="w-24 sm:w-48"
          alt="Blue Logo"
        />
        <img
          v-else
          src="../../assets/images/projects-logo-light.svg"
          class="w-24 sm:w-48"
          alt="White Logo"
        />
      </div>
    </div>
    <!-- Project image end -->

    <!-- Project details start -->
    <div class="w-full sm:w-3/4 text-left flex">
      <div class="mx-auto sm:mx-0 sm:flex sm:gap-10">
        <!-- Sitio project logo -->
        <a href="http://www.mysitio.co.uk">
          <img src="../../assets/images/Sitio_logo.svg" alt="" class="w-40 sm:w-42"/>
        </a>
        <!-- Project Avalanche logo -->
        <div class="mt-10 sm:mt-0">
          <a href="http://project-avalanche.surge.sh">
          <img
            src="../../assets/images/ProjectAvalanche.svg"
            alt=""
            type="button"
            class="cursor-pointer w-40 sm:w-52"
          />
          </a>
        </div>
      </div>
    </div>
    <!-- Project details end -->
  </div>
</template>

<script>
export default {

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
