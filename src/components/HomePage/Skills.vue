<!-- <template>
  <div class="flex items-center justify-center w-full skill-container border">
     //flex flex-col justify-center items-center 
    <div
      class="w-full xs:w-9/12 md:w-full mx-[4vw] md:mx-[15vw] border static-container justify-center items-center flex flex-col "
    >
      <h1 class="text-[40px] lg:text-[90px] text-[#F5EEE6] hide">
        What I'm really good at
      </h1>

      <div
        class="flex flex-col items-center justify-center px-10 py-6 pt-10 space-y-10 md:px-0 md:justify-start md:flex-row md:space-y-0 md:space-x-10 xl:space-x-12 2xl:space-x-14 3xl:space-x-16 border"
      >
        // Box 
        // hide 
        <div
          class="box flex flex-col w-full md:mx-0 md:w-[120px] md:h-[120px] 2md:w-[140px] 2md:h-[140px] lg:w-[150px] lg:h-[150px] xl:w-[180px] xl:h-[180px] 2xl:w-[200px] 2xl:h-[200px] "
          v-for="(item, index) in skillItems"
          :key="index"
        >
          // Content inside of the box
          <div
            class="flex flex-row items-stretch justify-center px-10 py-6 space-x-5 md:space-x-0 md:flex-col md:items-center md:px-6 md:py-6"
          >
            <div class="flex w-1/5 md:w-full md:items-center md:justify-center">
              <div
                class="item-container md:w-[50px] md:h-[50px] 2md:w-[60px] 2md:h-[60px] lg:w-[70px] lg:h-[70px] xl:w-[100px] xl:h-[100px] "
              >
                <img :src="item.src" class="object-contain w-full h-full" />
              </div>
            </div>
            <div
              class="flex items-center justify-start w-4/5 md:w-full md:justify-center  "
            >
              <h1 class="text-3xl">{{ item.title }}</h1>
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
          src: new URL(`../../assets/img/VueIcon.png`, import.meta.url),
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
  background: #181818;
  box-shadow: 0px 4px 50px 0px #f5eee6;
}

.static-container {
  min-height: 100vh;
  perspective: 900px;
  perspective-origin: 50% 50vh;
}
</style> -->
<template>
  <div class="flex items-center justify-center w-full skill-container  min-h-screen">
    
    <div
      class="w-full md:w-full mx-[4vw] justify-center items-center flex flex-col "
    >
      <h1 class="text-[12.5vw] xs:text-[50px] md:text-[80px] xl:text-[110px] 2xl:text-[120px] text-[#F5EEE6] hide">
        What I'm really good at
      </h1>

      <div
        class="flex flex-col items-center justify-center  px-10 py-10 space-y-10 md:px-0 md:justify-start md:flex-row md:space-y-0 md:space-x-10 xl:space-x-12 2xl:space-x-14 3xl:space-x-16 "
      >
        <!--  Box 
        hide  md:mx-0-->
        <div
          class="box flex flex-col w-full md:w-[150px] md:h-[150px] 2md:w-[160px] 2md:h-[160px] lg:w-[180px] lg:h-[180px] xl:w-[190px] xl:h-[190px] 2xl:w-[200px] 2xl:h-[200px] justify-center"
          v-for="(item, index) in skillItems"
          :key="index"
        >
          <!-- Content inside of the box -->
          <!-- flex flex-row items-stretch justify-center px-10 py-6 space-x-5 md:space-x-0 md:flex-col md:items-center md:px-6 md:py-6 2xl:space-y-5 border -->
          <div
            class="flex flex-row items-stretch justify-center px-10 py-6 space-x-5 md:space-x-0 md:flex-col md:items-center md:px-6 md:py-0 md:space-y-2  "
          >


            <div class="flex w-1/5 md:w-full md:items-center md:justify-center  ">

              <!-- item-container md:w-[50px] md:h-[50px] 2md:w-[60px] 2md:h-[60px] lg:w-[70px] lg:h-[70px] xl:w-[100px] xl:h-[100px] -->
              <!-- max-w-full xs:max-w-[80%] md:max-w-[80%] -->
              <div
                class="item-container md:w-[50px] md:h-[50px] 2md:w-[60px] 2md:h-[60px] lg:w-[70px] lg:h-[70px] xl:w-[100px] xl:h-[100px] "
              >
                <img :src="item.src" class="object-contain w-full h-full" />
              </div>
            </div>
            <div
              class="flex items-center justify-start w-4/5 md:w-full md:justify-center   "
            >
              <h1 class="text-3xl">{{ item.title }}</h1>
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
          src: new URL(`../../assets/img/VueIcon.png`, import.meta.url),
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
  background: #181818;
  box-shadow: 0px 4px 50px 0px #f5eee6;
}

/* .static-container {
  min-height: 100vh;
  perspective: 900px;
  perspective-origin: 50% 50vh;
} */
</style>