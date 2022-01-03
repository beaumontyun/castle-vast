<template>
  <transition name="fade">
    <div v-show="modal" class="fixed insert-0 mx-auto py-20 z-30 w-5/6">
      <!-- modal body -->
      <div
        v-show="modal"
        @click="showModal()"
        class="bg-filter bg-ternary-dark dark:bg-ternary-light bg-opacity-20"
      ></div>

      <!-- modal contents -->
      <main class="flex flex-col items-center justify-center">
        <transition name="fade-up-down">
          <div v-show="modal" class="modal-wrapper flex items-center z-30">
            <div
              class="
                modal
                mx-5
                bg-primary-dark
                shadow-lg
                flex-row
                rounded-lg
                relative
              "
            >
              <SitioDescription />
            </div>
          </div>
        </transition>
      </main>
    </div>
  </transition>
</template>

<script>
import SitioDescription from "./SitioDescription.vue";
export default {
  props: ["showModal", "modal"],
  components: {
    SitioDescription,
  },
};
</script>

<style>
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