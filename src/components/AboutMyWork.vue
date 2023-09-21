<template>
  <div class="flex flex-row items-stretch w-full pt-20">
    <div
      class="justify-center hidden -mt-[100px] xs:flex xs:w-3/12 md:w-1/4 lg:w-2/5 2xl:w-2/5 3xl:w-5/12"
    >
      <div
        ref="separatorBar"
        class="items-stretch w-5 h-full separatorBar"
      ></div>
      <div
        class="absolute w-12 h-12 cursor-pointer mt-[100px] separatorBox animate-glow"
      >
        <img
          src="../assets/img/SkillsIcon.png"
          class="object-contain w-full h-full px-2 py-2"
        />
      </div>
    </div>
    <div class="w-full xs:w-9/12 md:w-full 3xl:-ml-10">
      <h1 class="text-4xl">.AboutWork()</h1>

      <div
        class="flex flex-col items-center justify-center px-10 py-6 bg-gray-500 md:flex-row"
      >
        <div class="flex flex-col w-full bg-gray-600">
          <div>1</div>
          <div>2</div>
        </div>

        <div>bar</div>

        <div class="flex flex-col w-full bg-gray-600">
          <div>3</div>
          <div>4</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.separatorBar {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}
</style>
