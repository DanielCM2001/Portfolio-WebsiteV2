<template>
  <div class="flex items-center justify-center w-full">
    <!-- flex flex-col justify-center items-center -->
    <div class="w-full xs:w-9/12 md:w-full md:mx-[25vw] static-container">
      <h1 class="text-[40px] lg:text-[70px] 2xl:text-[80px] hide">
        What I'm really good at
      </h1>

      <div
        class="flex flex-col items-center justify-center px-10 py-6 pt-10 space-y-10 md:px-0 md:justify-start md:flex-row md:space-y-0 md:space-x-10 xl:space-x-12 2xl:space-x-14 3xl:space-x-16"
      >
        <!-- Box -->
        <div
          class="box flex flex-col w-full md:mx-0 md:w-[120px] md:h-[120px] 2md:w-[140px] 2md:h-[140px] lg:w-[150px] lg:h-[150px] xl:w-[180px] xl:h-[180px] hide"
          v-for="(item, index) in skillItems"
          :key="index"
        >
          <!-- Content inside of the box -->
          <div
            class="flex flex-row items-stretch justify-center px-10 py-6 space-x-5 md:space-x-0 md:flex-col md:items-center md:px-6 md:py-6"
          >
            <div class="flex w-1/5 md:w-full md:items-center md:justify-center">
              <div
                class="item-container md:w-[50px] md:h-[50px] 2md:w-[60px] 2md:h-[60px] lg:w-[70px] lg:h-[70px] xl:w-[100px] xl:h-[100px]"
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
    <!-- <h1
      class="text-center text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[40px] lg:text-[70px] 2xl:text-[80px] hide"
    >
      &lt;/Wrapper&gt;
    </h1> -->
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

/* class="relative p-[calc(50vh-3.5rem)] m-0 lg:m-0 xl:m-25vw min-h-screen perspective-900 perspective-origin-center lg:perspective-origin-50-top"> */
.static-container {
  padding: calc(50vh - 3.5rem) 0 0;
  min-height: 100vh;
  perspective: 900px;
  perspective-origin: 50% 50vh;
}
</style>
