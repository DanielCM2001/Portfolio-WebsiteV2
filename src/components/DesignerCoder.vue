<template>
  <div class="flex items-center justify-center w-full">
    <!-- ============================================= -->
    <div
      class="items-center justify-center hidden bg-gray-400 sm:flex sm:w-2/4 md:hidden"
    >
      <div class="w-5 h-[10px] separatorBar"></div>
    </div>
    <!-- ============================================= -->

    <div
      class="flex flex-col items-center justify-center w-full max-w-screen-2xl bg-slate-500 md:flex-row"
    >
      <!-- Left Side -->
      <div
        class="flex flex-col items-center justify-center w-full bg-slate-600 md:w-2/5 md:ml-5"
      >
        <p class="py-5 text-5xl DesignerText">Designer</p>

        <p class="text-lg">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et dolore
          magna aliqua. Ut enim ad minim veniam, qu
        </p>
      </div>

      <!-- Midle bar -->
      <div
        class="items-center justify-center hidden bg-gray-400 md:flex md:w-1/5"
      >
        <div class="w-5 h-[150px] separatorBar"></div>
      </div>
      <!-- =========== -->

      <!-- Right Side -->
      <div
        class="flex flex-col items-center justify-center w-full bg-slate-700 md:w-2/5 md:mr-5"
      >
        <p class="py-5 text-5xl">Coder</p>

        <p class="text-lg">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et dolore
          magna aliqua. Ut enim ad minim veniam, qu
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style scoped>
.DesignerText {
  background: linear-gradient(
    91deg,
    #c940eb 6.27%,
    #9b8df3 43.87%,
    #8c5dc9 80.87%
  );
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.separatorBar {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}
</style>
