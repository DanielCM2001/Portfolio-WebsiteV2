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
      <h1 class="text-4xl">.Work()</h1>

      <div
        class="flex flex-col mx-10 md:mx-0 md:w-[90%] my-6 bg-[#161b22] rounded-[10px] overflow-hidden border-[#30363d] border-[1px]"
      >
        <div class="flex flex-row pt-2 mx-2 space-x-5">
          <!-- translate-y-[1px] -->
          <div class="bg-[#24292f] py-1 px-2 rounded-t-lg">Working.vue</div>
          <div class="bg-[#161b22] py-1 px-2 rounded-t-lg">Working.js</div>
        </div>
        <div class="h-96 bg-[#24292f] border-[#30363d] border-t-[1px]">
          <div class="flex flex-row w-full bg-gray-700">
            <div class="px-2 bg-gray-800">1</div>
            <div>code..</div>
          </div>
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
