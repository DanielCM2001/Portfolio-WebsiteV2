<!-- <template>
  <div class="min-h-screen flex justify-center items-center">
    <div class="flex w-full">
      <div class="vertical-bar" :style="{ height: barHeight + 'px' }"></div>

      <div class="flex-1 w-1/2">
        <div class="w-1/2 bg-slate-600 flex justify-center items-center"></div>
        <div class="w-1/2 bg-slate-800 flex justify-center items-center">
          xd
        </div>
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
  width: 4px; 
  background-color: #c940eb;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 999;
  box-shadow: inset 0 0 10px rgba(201, 64, 235, 0.5),
    0 0 10px rgba(201, 64, 235, 0.5);
}

</style> -->

<template>
  <div class="min-h-screen flex justify-center items-center">
    <div class="flex justify-center items-center w-full flex-col md:flex-row">
      <div class="w-1/2">
        <div
          class="vertical-bar max-h-screen"
          :style="{ height: barHeight + 'px' }"
        ></div>
      </div>
      <div class="w-1/2 bg-slate-600 flex justify-center items-center">xd</div>

      <!-- <div class="flex-1 w-1/2">
        <div class="w-1/2 bg-slate-600 flex justify-center items-center"></div>
        <div class="w-1/2 bg-slate-800 flex justify-center items-center">
          xd
        </div>
      </div> -->
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
      this.barHeight = window.scrollY / 2;
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

<!-- <template>
  <div class="min-h-screen flex justify-center items-center">
    <div class="flex justify-center items-center w-full flex-row">
      <div class="w-1/2 bg-slate-600 flex justify-center items-center">
        <div class="bg-[#c940eb] w-20 absolute"></div>
      </div>
      <div class="w-1/2 bg-slate-800 flex justify-center items-center">xd</div>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script> -->
