<!-- <template>
  <div class="flex items-stretch justify-center w-full">
    <div
      class="flex flex-col items-stretch justify-center w-full max-w-screen-2xl xs:w-9/12"
    >
      <div class="py-10">
        <p class="text-2xl">What I did?</p>
        <p class="text-3xl glowLabel">Portfolio</p>
        <p class="text-4xl">Some of my projects...</p>
      </div>
    </div>

    <div class="bg-gray-800">Portfolio here</div>
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
 -->

<template>
  <div class="flex items-center justify-center w-full">
    <div
      class="w-full xs:w-9/12 md:w-full md:mx-[5vw] 2xl:mx-[15vw] static-container justify-center text-center items-center flex flex-col"
    >
      <div class="py-10">
        <!-- <p class="text-[40px] lg:text-[70px] 2xl:text-[60px]">What I did?</p> -->
        <!--  <p class="text-[40px] lg:text-[70px] glowLabel">Portfolio</p>
        <p class="text-[20px] lg:text-[50px] 2xl:text-[40px]">
          Some of my projects...
        </p> -->

        <!-- <p class="text-[30px]">What I did?</p>
        <p class="text-[45px] glowLabel">Portfolio</p> -->
        <h1
          class="text-[12.5vw] xs:text-[50px] md:text-[80px] xl:text-[110px] 2xl:text-[120px] text-[#F5EEE6]"
        >
          Some of my projects...
        </h1>
      </div>

      <div
        class="grid w-full gap-y-[20px] md:grid-cols-4 lg:grid-cols-8 md:grid-rows-2 md:gap-x-[40px] px-10"
      >
        <div
          class="box col-span-3 h-[300px] md:h-[320px] lg:h-[400px] 2xl:h-[500px] md:col-span-2 md:row-span-2"
        >
          <div class="front"></div>
        </div>
        <div
          class="box col-span-3 h-[300px] md:h-[150px] lg:h-[190px] 2xl:h-[240px] md:col-span-2"
        >
          <div class="front"></div>
        </div>
        <div
          class="box col-span-3 h-[300px] md:h-[320px] lg:h-[400px] 2xl:h-[500px] md:col-span-2 md:row-span-2"
        >
          <div class="front"></div>
        </div>
        <div
          class="box col-span-3 h-[300px] md:h-[150px] lg:h-[190px] 2xl:h-[240px] md:col-span-2"
        >
          <div class="front"></div>
        </div>

        <div
          class="box col-span-3 h-[300px] md:h-[150px] lg:h-[190px] 2xl:h-[240px] md:col-span-2"
        >
          <div class="front"></div>
        </div>
        <div
          class="box col-span-3 h-[300px] md:h-[150px] lg:h-[190px] 2xl:h-[240px] md:col-span-2"
        >
          <div class="front"></div>
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
.container {
  /*  perspective: 500px; */
}
.container:hover > .box {
  cursor: pointer;
  /*  transform: rotateY(180deg) rotateZ(180deg); */
  transform: rotateY(180deg);
}

.box {
  border-radius: 40px;
  background: #181818;
  box-shadow: 0px 4px 50px 0px #f5eee6;
  position: relative;
  transition: transform 1500ms;
  transform-style: preserve-3d;
}

.front,
.back {
  width: 100%;
  height: 100%;
  position: absolute;
  backface-visibility: hidden;
}
.front {
  border-radius: 40px;
  background-image: url("../../assets/img/Test.png");
  background-size: cover;
  background-repeat: no-repeat;
}
.back {
  border-radius: 40px;
  background: #151417;
  /* transform: rotateY(180deg) rotateZ(180deg); */
  transform: rotateY(180deg);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

/* class="relative p-[calc(50vh-3.5rem)] m-0 lg:m-0 xl:m-25vw min-h-screen perspective-900 perspective-origin-center lg:perspective-origin-50-top"> */
.static-container {
  /* padding: calc(50vh - 3.5rem) 0 0; */
  min-height: 100vh;
  perspective: 900px;
  perspective-origin: 50% 50vh;
}
.glowLabel {
  color: #c3023a;
  text-shadow: 0px 4px 50px #c3023a;
}
</style>
