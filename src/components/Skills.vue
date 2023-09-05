<!-- <template>
  <div class="min-h-screen flex justify-center items-center flex-col">
    <div class="flex justify-center items-center w-full flex-col bg-gray-800">
      <h1 class="text-5xl">What I'm really good at</h1>
      <div
        class="w-full bg-black flex justify-center items-center flex-col space-y-20 lg:flex-row lg:space-x-20 lg:space-y-0"
      >
        <div class="box"></div>
        <div class="box"></div>
        <div class="box"></div>
        <div class="box"></div>
      </div>
    </div>
  </div>
</template> -->

<template>
  <div class="flex justify-center items-center flex-row bg-gray-700">
    <div class="w-0 md:w-1/4 flex justify-center items-center">linha</div>
    <div class="w-full md:w-3/4 bg-gray-900">
      <h1 class="text-4xl">What I'm really good at</h1>
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
.box {
  border-radius: 40px;
  background: #313339;
  box-shadow: 0px 5px 5px 0px #8c5dc9 inset, 0px 4px 40px 0px #c940eb;
}
</style>
