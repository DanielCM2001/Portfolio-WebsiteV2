<!-- <section class="flex flex-col items-center justify-center h-[100vh] w-full">
    <div
      class="z-20 flex items-center justify-center w-full mt-20 border h-1/2"
    >
      <h1 class="uppercase text-[35px]">
        I AM A FRONT END <br />
        DEVELOPER
      </h1>
    </div>

    <div class="absolute flex items-center justify-center w-full h-full border">
      <img
        src="../../assets/img/BannerCircle.png"
        alt="Banner image"
        class="w-full max-w-xl"
      />
    </div>

    
    <div class="flex flex-col items-center justify-center w-full border h-1/2">
      <div class="mt-20">
        <h1 class="text-2xl">Hi there! I'm Daniel</h1>
        <h1 class="text-2xl">
          Passionate about creating interactive applications and experiences on
          the web.
        </h1>
      </div>
    </div>
  </section> -->

<template>
  <section class="flex items-center justify-center h-[100vh] w-full">
    <!-- <div
      class="z-20 flex items-center justify-center w-full mt-20 border h-1/2"
    >
      <h1 class="uppercase text-[35px]">
        I AM A FRONT END <br />
        DEVELOPER
      </h1>
    </div>

    <div class="absolute flex items-center justify-center w-full h-full border">
      <img
        src="../../assets/img/BannerCircle.png"
        alt="Banner image"
        class="w-full max-w-xl"
      />
    </div> -->

    <div
      class="flex items-start justify-center w-full h-[100vh] text-center border"
    >
      <div class="flex flex-col items-center justify-center pt-40">
        <h1 class="uppercase text-[100px]">
          I AM A FRONT END <br />
          DEVELOPER
        </h1>
        <img
          src="../../assets/img/BannerCircle.png"
          alt="Banner image"
          class="w-full max-w-xl -mt-40"
        />
      </div>

      <div class="absolute bottom-[30%] left-0">
        <h1 class="text-2xl">
          Passionate about creating interactive applications and experiences on
          the web.
        </h1>
      </div>

      <!--   <div
        class="absolute flex items-start justify-center w-full h-full pt-40 border"
      >
        <img
          src="../../assets/img/BannerCircle.png"
          alt="Banner image"
          class="w-full max-w-xl"
        />
      </div> -->
    </div>
  </section>
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
