<template>
  <div class="container mx-auto">
    <div
      class="
        innercontent
        pt-20
        sm:pt-30
        pb-1
        mt-20
        border-t-2 border-primary-light
        dark:border-secondary-dark
      "
    >
      <!-- Footer social links start -->
      <div class="flex flex-col sm:justify-center sm:items-center mb-1 sm:mb-10">
        <div class="grid sm:grid-cols-1 grid-cols-3 text-left">
          <p
            class="
              sm:hidden
              font-medium
              text-blue-900
              dark:text-primary-light
              mb-5
            "
          >
            CONTACT
          </p>
          <ul class="text-xs sm:text-base mb-4 sm:flex gap-1 sm:gap-8 col-span-2">
            <p class="sm:mb-4 text-ternary-dark dark:text-ternary-light">
              +852 6279 6046
            </p>
            <a class="mb-4 text-ternary-dark dark:text-ternary-light"
              >corporate@castle-vast.com</a
            >
          </ul>
        </div>
        <div class="mb-4 text-xs sm:text-sm flex justify-center items-center text-center">
          <div class="text-ternary-dark dark:text-ternary-light">
            &copy; Copyright {{ copyrightDate }}. Castle Vast Limited, Hong Kong
            SAR.
          </div>
        </div>
      </div>
      <!-- Footer social links end -->

      <!-- Footer copyright start -->

      <!-- Footer copyright end -->
    </div>
  </div>
</template>

<script>
import feather from "feather-icons";
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
