<template>
  <div class="flex flex-col items-center justify-center min-h-screen">
    <div class="flex flex-col items-center justify-center w-full md:flex-row">
      <div
        class="flex flex-col w-full md:items-center md:justify-center lg:w-1/2"
      >
        <div
          class="w-full pl-5 pr-5 space-y-20 2xl:space-y-40 md:pr-0 lg:w-4/5 lg:pl-0 2xl:w-3/5"
        >
          <!-- Fix later the Hide class and JS sense It's overlapping the navbar -->
          <div class="mt-20 space-y-10 md:mt-24 hide">
            <h1 class="text-4xl">Hi there! I'm Daniel</h1>
            <p class="text-2xl">
              A front-end Web Developer passionate about creating interactive
              applications and experiences on the web.
            </p>

            <!--  <div class="flex flex-row space-x-5 text-lg sm:space-x-10 hide">
              <button class="px-8 py-3 primaryButtons">Download</button>
              <button class="px-5 py-3 primaryButtons">xd</button>
              <button class="px-5 py-3 primaryButtons">xd</button>
            </div> -->

            <div class="flex flex-row space-x-5 text-lg sm:space-x-10 hide">
              <button class="px-5 py-3 primaryButtons">xd</button>
              <button class="px-5 py-3 primaryButtons">xd</button>
              <button class="px-5 py-3 primaryButtons">xd</button>
            </div>
          </div>

          <div
            class="flex flex-col px-10 py-4 space-y-5 InfoBox xs:mr-10 sm:flex-row sm:space-y-0 sm:space-x-5 sm:mr-5 lg:-mr-10 max-w-7xl hide"
          >
            <div
              class="flex flex-row w-full space-x-5 sm:flex-col sm:space-x-0"
            >
              <p class="text-5xl md:text-4xl lg:text-5xl">+8</p>
              <p class="text-lg md:text-md lg:text-lg">Projects completed</p>
            </div>

            <div class="w-full h-1 sm:h-28 sm:w-5 separatorBar"></div>

            <div
              class="flex flex-row w-full space-x-5 sm:flex-col sm:space-x-0"
            >
              <p class="text-5xl md:text-4xl lg:text-5xl">2</p>
              <p class="text-lg md:text-md lg:text-lg">Years of Experience</p>
            </div>

            <div class="w-full h-1 sm:h-28 sm:w-5 separatorBar"></div>

            <div
              class="flex flex-row w-full space-x-5 sm:flex-col sm:space-x-0"
            >
              <p class="text-5xl md:text-4xl lg:text-5xl">100%</p>
              <p class="text-lg md:text-md lg:text-lg">Of Happy Clients</p>
            </div>
          </div>
        </div>
      </div>

      <div
        class="relative flex items-center justify-end w-full mt-20 md:mt-0 lg:w-1/2"
      >
        <img
          src="../../assets/img/BannerRectangle.png"
          alt="Banner image"
          class="w-full max-w-2xl"
        />

        <img
          src="../../assets/img/AvatarBigger.png"
          alt="Banner image"
          class="w-full max-w-[650px] absolute top-0 animateAvatar"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style scoped>
.animateAvatar {
  animation: avatar 1.5s infinite alternate; /* animation */
}
@keyframes avatar {
  0% {
    transform: translateY(0px);
  }
  100% {
    transform: translateY(-10px);
  }
}

.primaryButtons {
  border-radius: 20px;
  background: #c3023a;
  box-shadow:
    0px 5px 5px 0px #c3023a inset,
    0px 4px 50px 0px #c3023a;
}
.InfoBox {
  border-radius: 30px;
  background: #141414;
  box-shadow:
    0px 5px 5px 0px #c3023a inset,
    0px 4px 50px 0px #c3023a;
}

.separatorBar {
  border-radius: 20px;
  background: #c3023a;
  box-shadow:
    0px 5px 5px 0px #c3023a inset,
    0px 4px 50px 0px #c3023a;
}
</style>
