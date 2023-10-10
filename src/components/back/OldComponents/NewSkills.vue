<template>
  <div class="flex flex-row w-full min-h-screen">
    <div
      class="items-center justify-center hidden xs:flex xs:w-3/12 md:w-1/4 lg:w-2/5 2xl:w-2/5 3xl:w-4/12"
    >
      <div class="relative items-stretch w-5 h-full separator-container hide">
        <div class="top-separator"></div>
        <div class="bottom-separator"></div>
      </div>
      <div class="absolute w-12 h-12 cursor-pointer separatorBox animate-glow">
        <img
          src="../assets/img/SkillsIcon.png"
          class="object-contain w-full h-full px-2 py-2"
        />
      </div>
    </div>

    <div class="flex flex-col justify-center w-full xs:w-9/12 md:w-full">
      <h1 class="text-[40px] lg:text-[70px] 2xl:text-[80px] hide">
        What I'm really good at
      </h1>

      <div
        class="flex flex-col items-center justify-center px-10 py-6 pt-10 space-y-10 md:px-0 md:justify-start md:flex-row md:space-y-0 md:space-x-10 xl:space-x-12 2xl:space-x-14 3xl:space-x-16"
      >
        <!-- Box -->
        <div
          class="box flex flex-col w-full md:mx-0 md:w-[120px] md:h-[120px] 2md:w-[140px] 2md:h-[140px] lg:w-[150px] lg:h-[150px] xl:w-[160px] xl:h-[160px] hide"
          v-for="(item, index) in skillItems"
          :key="index"
        >
          <!-- Content inside of the box -->
          <div
            class="flex flex-row items-stretch justify-center px-10 py-6 space-x-5 md:space-x-0 md:flex-col md:items-center md:px-6 md:py-6"
          >
            <div class="flex w-1/5 md:w-full md:items-center md:justify-center">
              <div
                class="item-container md:w-[50px] md:h-[50px] 2md:w-[60px] 2md:h-[60px] lg:w-[70px] lg:h-[70px] xl:w-[80px] xl:h-[80px]"
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
      barWidth: 0,
      LeftWidthOfVerticalBar: 0,
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
/* .box {
    border-radius: 40px;
    background: rgb(246, 245, 245);
    color: #131313;
    box-shadow:
      0px 3px 3px 0px #8c5dc9 inset,
      0px 4px 40px 0px #c940eb;
  } */

.separatorBar {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 30px 0px #c940eb;
}

.separatorHorizontalBar {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}

.separator-container {
  position: relative;
  height: 100%;
  width: 5px;
}

.top-separator {
  top: 0;
  opacity: 0.5;
}

.bottom-separator {
  bottom: 0;
}

.bottom-separator,
.top-separator {
  position: absolute;

  left: 50%;
  transform: translateX(-50%);
  width: 10px; /* Width for the bottom portion */
  height: 50%;
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 30px 0px #c940eb;
}
</style>
