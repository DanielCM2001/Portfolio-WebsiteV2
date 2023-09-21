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
        class="flex flex-col items-stretch justify-center px-10 py-6 md:w-full md:flex-row md:px-0 xl:w-[90%] 2xl:w-[80%] 3xl:w-[70%]"
      >
        <div class="flex flex-col w-full">
          <div class="flex flex-col justify-center">
            <p class="py-5 text-2xl glowLabel">Designer</p>

            <p class="text-lg">
              Fast load times and lag-free interaction, my highest priority.
            </p>
          </div>
          <div class="flex flex-col justify-center">
            <p class="py-5 text-2xl glowLabel">Responsive</p>

            <p class="text-lg">
              My layouts will work on any device, big or small.
            </p>
          </div>
        </div>

        <div class="justify-center hidden md:flex md:w-1/5">
          <div class="w-5 h-full separatorBar"></div>
        </div>

        <div class="flex flex-col w-full">
          <div class="flex flex-col justify-center">
            <p class="py-5 text-2xl glowLabel">Dynamic</p>

            <p class="text-lg">
              Websites don't have to be static, I love making pages come to
              life.
            </p>
          </div>
          <div class="flex flex-col justify-center">
            <p class="py-5 text-2xl glowLabel">Intuitive</p>

            <p class="text-lg">
              Strong preference for easy to use, intuitive UX/UI.
            </p>
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
.glowLabel {
  color: #c940eb;
  text-shadow: 0px 4px 50px #c940eb;
}
.separatorBar {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}
</style>
