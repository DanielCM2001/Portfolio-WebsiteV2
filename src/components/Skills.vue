<!-- <template>
  <div class="flex flex-row items-center justify-center">
    <div class="items-center justify-center hidden md:flex md:w-1/4">linha</div>
    <div class="w-full md:w-3/4">
      <h1 class="text-4xl">What I'm really good at</h1>

      <div
        class="flex flex-col items-center justify-center py-10 space-y-10 lg:justify-start lg:flex-row lg:space-y-0 lg:space-x-20"
      >
        <div
          v-for="(item, index) in skillItems"
          :key="index"
          class="box w-[200px] h-[200px] lg:w-[140px] lg:h-[140px] xl:w-[160px] xl:h-[160px]"
        >
          <div class="flex flex-col items-center justify-center px-8 py-8">
            <img :src="item.src" class="w-full" />
            <h1 class="text-xl">{{ item.title }}</h1>
          </div>
        </div>
      </div>
    </div>
  </div>
</template> -->

<template>
  <div class="flex flex-row items-center justify-center">
    <div
      class="items-center justify-center hidden bg-gray-700 sm:flex sm:w-2/4"
    >
      <div class="w-5 h-[10px] separatorBar"></div>
    </div>
    <div class="w-full md:w-3/4">
      <h1 class="text-4xl">What I'm really good at</h1>

      <div
        class="flex flex-col items-center justify-center py-10 space-y-10 lg:justify-start lg:flex-row lg:space-y-0 lg:space-x-20"
      >
        <div
          v-for="(item, index) in skillItems"
          :key="index"
          class="box w-[200px] h-[200px] lg:w-[140px] lg:h-[140px] xl:w-[160px] xl:h-[160px]"
        >
          <div class="flex flex-col items-center justify-center px-8 py-8">
            <div
              class="item-container w-[120px] h-[120px] lg:w-[50px] lg:h-[50px] xl:w-[80px] xl:h-[80px]"
            >
              <img :src="item.src" class="object-contain w-full h-full" />
            </div>
            <h1 class="text-xl">{{ item.title }}</h1>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      skillItems: [
        {
          src: new URL(`@/assets/img/VueIcon.png`, import.meta.url),
          title: "Vue.JS",
        },
        {
          src: new URL(`@/assets/img/ReactIcon.png`, import.meta.url),
          title: "React",
        },
        {
          src: new URL(`@/assets/img/ReactIcon.png`, import.meta.url),
          title: "Design",
        },
        {
          src: new URL(`@/assets/img/OtherIcon.png`, import.meta.url),
          title: "Other",
        },
      ],
    };
  },
};
</script>

<style scoped>
.box {
  border-radius: 40px;
  background: #2d2d31;
  box-shadow:
    0px 3px 3px 0px #8c5dc9 inset,
    0px 4px 40px 0px #c940eb;
}

.separatorBar {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}
</style>
