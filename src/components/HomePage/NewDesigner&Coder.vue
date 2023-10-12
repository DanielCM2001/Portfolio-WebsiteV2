<template>
  <div
    class="flex items-stretch justify-center w-full min-h-screen designerCoder"
  >
    <div
      class="flex flex-col items-stretch justify-center w-full pl-5 pr-5 max-w-screen-2xl md:flex-row md:space-x-10"
    >
      <!-- Left Side -->
      <div class="flex flex-col items-center justify-center w-full text-center">
        <p
          class="py-5 text-[70px] lg:text-[90px] 2xl:text-[120px] DesignerText hide"
        >
          Designer
        </p>

        <p class="text-xl lg:text-2xl 2xl:text-3xl hide">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et dolore
          magna aliqua. Ut enim ad minim veniam, qu
        </p>
      </div>

      <!-- Midle bar -->
      <!--  <div class="justify-center hidden -mb-[20px] md:flex md:w-1/5">
        <div class="w-5 h-full separatorBar"></div>
        <div
          class="absolute w-12 h-12 cursor-pointer separatorBox animate-glow"
        >
          <img
            src="../assets/img/IdeasIcon.png"
            class="object-contain w-full h-full px-2 py-2"
          />
        </div>
      </div> -->

      <!-- Right Side -->
      <div class="flex flex-col items-center justify-center w-full text-center">
        <p class="py-5 text-[70px] lg:text-[90px] 2xl:text-[120px] hide">
          Coder++
        </p>

        <p class="text-xl lg:text-2xl 2xl:text-3xl hide">
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
</style>
