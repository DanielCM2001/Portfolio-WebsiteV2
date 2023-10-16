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
      class="w-full xs:w-9/12 md:w-full md:mx-[15vw] static-container justify-center text-center items-center flex flex-col"
    >
      <div class="py-10">
        <p class="text-4xl">What I did?</p>
        <p class="text-3xl glowLabel">Portfolio</p>
        <p class="text-2xl">Some of my projects...</p>
      </div>

      <!--    <div
        class="flex flex-col items-center justify-center w-full space-x-10 bg-gray-800 lg:flex-row"
      >
        <div class="w-52 h-[340px] box bg-img"></div>
        <div class="flex-col space-y-[20px]">
          <div class="h-40 w-52 box bg-img"></div>
          <div class="h-40 w-52 box bg-img"></div>
        </div>
        <div class="w-52 h-[340px] box bg-img"></div>
        <div class="flex-col space-y-[20px]">
          <div class="h-40 w-52 box bg-img"></div>
          <div class="h-40 w-52 box bg-img"></div>
        </div>
      </div> -->

      <div
        class="container flex flex-col items-center justify-center w-full px-10 py-6 space-y-10 lg:flex-row"
      >
        <div class="w-full h-[320px] box">
          <div class="front"></div>
          <div class="space-y-5 back">
            <h1 class="text-2xl">Business Website</h1>
            <p class="text-lg">Design & Development of a company's website</p>
          </div>
        </div>
        <!--     <div class="w-full h-[320px] box bg-img"></div>
        <div class="w-full h-[320px] box bg-img"></div>
        <div class="w-full h-[320px] box bg-img"></div>
        <div class="w-full h-[320px] box bg-img"></div>
        <div class="w-full h-[320px] box bg-img"></div> -->
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
  background: #151417;
  box-shadow:
    0px 3px 3px 0px #8c5dc9 inset,
    0px 4px 40px 0px #c940eb;
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
  color: #c940eb;
  text-shadow: 0px 4px 50px #c940eb;
}
</style>
