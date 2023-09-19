<template>
  <div class="flex flex-row items-stretch w-full pt-20">
    <div
      class="justify-center hidden xs:flex xs:w-3/12 md:w-1/4 lg:w-2/5 2xl:w-2/5 3xl:w-5/12"
    >
      <div class="items-stretch w-5 h-full separatorBar"></div>
      <div class="absolute w-12 h-12 separatorBox animate-glow cursor-pointer">
        <img
          src="../assets/img/SkillsIcon.png"
          class="object-contain w-full h-full py-2 px-2"
        />
      </div>
    </div>
    <div class="w-full xs:w-9/12 md:w-full 3xl:-ml-10">
      <h1 class="text-4xl">What I'm really good at</h1>

      <div
        class="flex flex-col items-center justify-center px-10 py-6 space-y-10 md:px-0 md:justify-start md:flex-row md:space-y-0 md:space-x-10 xl:space-x-12"
      >
        <!-- Box -->
        <div
          class="box flex flex-col w-full md:mx-0 md:w-[120px] md:h-[120px] lg:w-[160px] lg:h-[160px]"
          v-for="(item, index) in skillItems"
          :key="index"
        >
          <!-- Content inside of the box -->
          <div
            class="flex flex-row items-stretch justify-center px-10 py-6 space-x-5 md:space-x-0 md:flex-col md:items-center md:px-6 md:py-6"
          >
            <div class="flex w-1/5 md:w-full md:items-center md:justify-center">
              <div
                class="item-container md:w-[50px] md:h-[50px] lg:w-[80px] lg:h-[80px]"
              >
                <img :src="item.src" class="object-contain w-full h-full" />
              </div>
            </div>
            <div
              class="flex items-center justify-start w-4/5 md:w-full md:justify-center"
            >
              <h1 class="text-xl">{{ item.title }}</h1>
            </div>
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
          src: new URL(`@/assets/img/JavascriptIcon.png`, import.meta.url),
          title: "Javascript",
        },
        {
          src: new URL(`@/assets/img/FigmaIcon.png`, import.meta.url),
          title: "Figma",
        },
      ],
    };
  },
};
</script>

<style scoped>
.box {
  border-radius: 40px;
  background: #151417;
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
.separatorBox {
  border-radius: 15px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
  animation: glow 1.5s infinite alternate; /* Glowing animation */
}

@keyframes glow {
  0% {
    box-shadow: 0 0 5px #c940eb; /* Initial glow effect */
  }
  100% {
    box-shadow: 0 0 30px #c940eb; /* Stronger glow effect */
  }
}
</style>
