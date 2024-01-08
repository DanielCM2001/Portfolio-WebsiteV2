<template>
  <section class="w-full pt-[20vh] flex flex-col text-center">
    <h1
      class="secondaryFont uppercase text-[#C7C8BF] font-semibold text-[180px] leading-tight"
    >
      Designer <span class="text-[110px] font-semibold uppercase">&</span>
    </h1>
    <h1
      class="secondaryFont uppercase text-[#C7C8BF] font-semibold text-[180px] leading-tight"
    >
      Developer
    </h1>
    <h2 class="text-[60px] font-bold">Hello I'm Daniel.</h2>

    <div class="flex flex-row justify-center items-center space-x-10">
      <a
        class="relative py-[.40rem] px-[2rem] rounded-[2rem] border border-[#cbc8c4] text-[#C7C8BF]"
        href="#contact"
        ><span class="font-bold text-[30px]">Let's talk</span></a
      >
      <a
        class="relative py-[.40rem] px-[2rem] rounded-[2rem] bg-[#C7C8BF] text-[#131313]"
        href="#contact"
        ><span class="font-bold text-[30px]">About me</span></a
      >
    </div>

    <!-- Right side scroll down -->
    <div
      class="absolute bottom-12 right-0 flex flex-col items-center justify-center space-y-8"
      style="opacity: 1"
    >
      <span class="rotate-90 text-body-3">scroll</span>
      <div
        class="relative h-1 w-10 rotate-90 overflow-hidden animation bg-[#C7C8BF]"
      >
        <span
          class="absolute h-[0.08em] w-10 translate-x-10 bg-accent-300"
        ></span>
      </div>
    </div>
    <!-- <div class="py-[10vh] justify-center flex relative">
      <div class="relative">
        <img
          src="../../assets/img/SquareArtMichaelAngelo.png"
          class="h-[100vh]"
        />
        <svg
          viewBox="0 0 100 100"
          width="100"
          height="100"
          class="absolute -right-[5%] top-[20px] bg-[#F5EEE6] rounded-full text-[#131313]"
        >
          <defs>
            <path
              id="circle"
              d="
        M 50, 50
        m -37, 0
        a 37,37 0 1,1 74,0
        a 37,37 0 1,1 -74,0"
            />
          </defs>
          <text font-size="17">
            <textPath xlink:href="#circle" class="uppercase font-medium">
              scroll down for more
            </textPath>
          </text>
        </svg>
      </div>
    </div> -->
  </section>
</template>

<script>
export default {
  mounted() {},
};
</script>

<style scoped>
svg {
  fill: currentColor;
  height: auto;
  max-width: 10vmin;
  transform-origin: center;
  width: 66%;
  padding: 5px;

  animation-duration: 4s;
  animation-iteration-count: infinite;
  animation-name: identifier;
}

@keyframes identifier {
  0% {
    rotate: 0deg;
  }
  100% {
    rotate: 360deg;
  }
}
</style>
