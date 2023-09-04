<template>
  <div class="min-h-screen flex justify-center items-center">
    <div class="flex justify-center items-center w-full flex-col md:flex-row">
      <div
        class="w-full lg:w-1/4 bg-slate-600 flex justify-center items-center"
      >
        <div
          class="vertical-bar max-h-screen"
          :style="{ height: barHeight + 'px' }"
        ></div>
      </div>
      <div
        class="w-full lg:w-3/4 bg-slate-600 flex justify-center items-center"
      >
        xd
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      barHeight: 0,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.updateBarHeight);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.updateBarHeight);
  },
  methods: {
    updateBarHeight() {
      this.barHeight = window.scrollY;
    },
  },
};
</script>

<style scoped>
.vertical-bar {
  /* width: 4px;
  background-color: #c940eb;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 999;
  box-shadow: inset 0 0 10px rgba(201, 64, 235, 0.5),
    0 0 10px rgba(201, 64, 235, 0.5); */

  width: 4px;
  background-color: #c940eb;
  /*  position: fixed;
  top: 0;
  left: 0; z-index: 999;
 */

  box-shadow: inset 0 0 10px rgba(201, 64, 235, 0.5),
    0 0 10px rgba(201, 64, 235, 0.5);
}
</style>
