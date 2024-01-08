<template>
  <section>
    <!--  <div
      class="h-[100vh] flex items-center justify-center flex-col space-y-5 relative"
    >
      <h1 class="text-[40px] lg:text-[70px]">About my work</h1>
      <div
        class="flex flex-col items-center justify-center px-10 py-6 pt-10 space-y-10 md:px-0 md:justify-start md:flex-row md:space-y-0 md:space-x-10 xl:space-x-12 2xl:space-x-14 3xl:space-x-16"
      >
        <div
          class="box flex flex-col w-full md:mx-0 xl:w-[300px] xl:h-[330px] hide"
          v-for="(item, index) in skillItems"
          :key="index"
        >
          <div
            class="flex flex-row items-stretch justify-center px-10 py-6 space-x-5 space-y-5 text-center md:space-x-0 md:flex-col md:items-center md:px-6 md:py-6"
          >
            <div class="item-container xl:w-[100px] xl:h-[100px]">
              <h1 class="text-5xl">LOGO</h1>
            </div>

            <h1
              class="text-2xl text-[#C3023A] font-bold [text-shadow:0_4px_50px_rgba(195,2,58,1)]"
            >
              {{ item.title }}
            </h1>

            <h1 class="text-xl">
              {{ item.description }}
            </h1>
          </div>
        </div>
      </div>
      <div class="arrow"></div>
    </div> -->
    <!--  <div
      class="h-[50vh] newskycontainer flex items-end justify-center relative"
    >
      <h1
        class="text-center secondaryFont text-[#f5eee6] text-[40px] lg:text-[70px] 2xl:text-[80px] hide"
      >
        &lt;Wrapper&gt;
      </h1>
    </div> -->

    <!--  <SpaceScene /> -->
    <SkyScene />
  </section>
</template>

<script>
import SkyScene from "./AnimatedScenes/SkyAnimated.vue";

export default {
  data() {
    return {
      barWidth: 0,
      LeftWidthOfVerticalBar: 0,
      skillItems: [
        {
          src: new URL(`../../assets/img/VueIcon.png`, import.meta.url),
          title: "Vue.JS",
          description:
            "Fast load times and lag free interaction, my highest priority.",
        },
        {
          src: new URL(`../../assets/img/VueIcon.png`, import.meta.url),
          title: "Dynamic",
          description:
            "Websites don't have to be static, I love making pages come to life.",
        },
        {
          src: new URL(`../../assets/img/VueIcon.png`, import.meta.url),
          title: "Responsive",
          description: "My layouts will work on any device, big or small.",
        },
        {
          src: new URL(`../../assets/img/VueIcon.png`, import.meta.url),
          title: "Intuitive",
          description: "Strong preference for easy to use, intuitive UX/UI.",
        },
      ],
    };
  },
  setup() {
    return {};
  },
  components: {
    SkyScene,
  },
};
</script>

<style scoped>
.box {
  /*  border-radius: 40px;
  background: #c940eb;
  box-shadow:
    0px 3px 3px 0px #8c5dc9 inset,
    0px 4px 40px 0px #c940eb; */
  border-radius: 40px;
  background: #141416;
  box-shadow:
    0px 3px 3px 0px #c3023a inset,
    0px 4px 40px 0px #c3023a;
}

/* class="relative p-[calc(50vh-3.5rem)] m-0 lg:m-0 xl:m-25vw min-h-screen perspective-900 perspective-origin-center lg:perspective-origin-50-top"> */
.static-container {
  /* padding: calc(50vh - 3.5rem) 0 0; */
  min-height: 100vh;
  perspective: 900px;
  perspective-origin: 50% 50vh;
}

.arrow,
.arrow:before {
  position: absolute;
  left: 50%;
}
.arrow {
  width: 40px;
  height: 40px;
  top: 110%;
  margin: -20px 0 0 -20px;
  -webkit-transform: rotate(45deg);
  border-left: none;
  border-top: none;
  border-right: 2px #c3023a solid;
  border-bottom: 2px #c3023a solid;
}
.arrow:before {
  content: "";
  width: 20px;
  height: 20px;
  top: 50%;
  margin: -10px 0 0 -10px;
  border-left: none;
  border-top: none;
  border-right: 1px #c3023a solid;
  border-bottom: 1px #c3023a solid;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  animation-name: arrow;
}
@keyframes arrow {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
    transform: translate(-10px, -10px);
  }
}
</style>
