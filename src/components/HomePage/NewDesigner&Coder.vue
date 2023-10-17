<template>
  <div
    class="flex items-stretch justify-center w-full min-h-screen designerCoder bg-gradient-to-b text-white from-[#03A9F4] from-0% to-[#66B7DC] to-80%"
  >
    <div
      class="flex flex-col items-stretch justify-center w-full pl-5 pr-5 max-w-screen-2xl md:flex-row md:space-x-10"
    >
      <!-- Left Side -->
      <div class="flex flex-col items-center justify-center w-full text-center">
        <p class="py-5 text-[70px] lg:text-[90px] 2xl:text-[120px] hide">
          Designer
        </p>

        <p class="text-xl lg:text-2xl 2xl:text-3xl hide">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et dolore
          magna aliqua. Ut enim ad minim veniam, qu
        </p>
      </div>

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
