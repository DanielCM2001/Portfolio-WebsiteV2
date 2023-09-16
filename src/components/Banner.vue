<template>
  <div class="flex flex-col items-center justify-center min-h-screen">
    <div class="flex flex-col items-center justify-center w-full md:flex-row">
      <div
        class="flex flex-col w-full md:items-center md:justify-center lg:w-1/2"
      >
        <!-- Changed Space-y-40 -->
        <div
          class="w-full pl-5 pr-5 space-y-20 2xl:space-y-40 md:pr-0 lg:w-4/5 lg:pl-0 2xl:w-3/5"
        >
          <!-- ADDED THE DIV BELOW -->
          <!-- space-y-10 mt-20 md:mt-40 -->
          <div class="mt-20 space-y-10 md:mt-40">
            <h1 class="text-5xl">Hi there! I'm Daniel</h1>
            <p class="text-2xl">
              A front-end Web Developer passionate about creating interactive
              applications and experiences on the web.
            </p>

            <div class="flex flex-row space-x-5 text-lg sm:space-x-10">
              <!-- glow-on-hover -->
              <button class="px-8 py-3 primaryButtons">LinkedIn</button>
              <button class="px-5 py-3 primaryButtons">Icon</button>
              <button class="px-5 py-3 primaryButtons">Icon</button>
            </div>
          </div>

          <div
            class="flex flex-col px-10 py-6 mr-5 space-y-5 InfoBox xs:mr-10 sm:flex-row sm:space-y-0 sm:space-x-5 sm:mr-5 lg:-mr-10 max-w-7xl"
          >
            <div
              class="flex flex-row w-full space-x-5 sm:flex-col sm:space-x-0"
            >
              <p class="text-5xl md:text-4xl lg:text-5xl">+5</p>
              <p class="text-lg md:text-md lg:text-lg">Lorem Ipsum dolor</p>
            </div>

            <div class="w-full h-1 sm:h-28 sm:w-5 separatorBar"></div>

            <div
              class="flex flex-row w-full space-x-5 sm:flex-col sm:space-x-0"
            >
              <p class="text-5xl md:text-4xl lg:text-5xl">60%</p>
              <p class="text-lg md:text-md lg:text-lg">Lorem Ipsum dolor</p>
            </div>

            <div class="w-full h-1 sm:h-28 sm:w-5 separatorBar"></div>

            <div
              class="flex flex-row w-full space-x-5 sm:flex-col sm:space-x-0"
            >
              <p class="text-5xl md:text-4xl lg:text-5xl">100</p>
              <p class="text-lg md:text-md lg:text-lg">Lorem Ipsum dolor</p>
            </div>
          </div>
        </div>
      </div>
      <div class="flex justify-end w-full mt-20 md:mt-0 lg:w-1/2">
        <img
          src="../assets/img/BannerRectangle.png"
          alt="Banner image"
          class="w-full max-w-2xl"
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
.primaryButtons {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}
.InfoBox {
  border-radius: 30px;
  background: #151417;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}

.separatorBar {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}

/* ===================================== */
/* .glow-on-hover:before { */
/*  background: linear-gradient(
    45deg,
    #ff0000,
    #ff7300,
    #fffb00,
    #48ff00,
    #00ffd5,
    #002bff,
    #7a00ff,
    #ff00c8,
    #ff0000
  ); */
/* 
.glow-on-hover {
  border: none;
  outline: none;
  background: #c940eb;
  cursor: pointer;
  position: relative;
  z-index: 0;
}

.glow-on-hover:before {
  content: "";

  background: linear-gradient(
    45deg,
    #c940eb,
    #9d32b7,
    #5b1d6a,
    #8c5dc9,
    #4c2259
  );
  position: absolute;
  top: -2px;
  left: -2px;
  background-size: 400%;
  z-index: -1;
  filter: blur(5px);
  width: calc(100% + 4px);
  height: calc(100% + 4px);
  animation: glowing 20s linear infinite;
  opacity: 0;
  transition: opacity 0.3s ease-in-out;
  border-radius: 10px;
}

.glow-on-hover:active {
  color: #000;
}

.glow-on-hover:active:after {
  background: transparent;
}

.glow-on-hover:hover:before {
  opacity: 1;
}

.glow-on-hover:after {
  z-index: -1;
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background: #c940eb;
  left: 0;
  top: 0;
  border-radius: 10px;
}

@keyframes glowing {
  0% {
    background-position: 0 0;
  }
  50% {
    background-position: 400% 0;
  }
  100% {
    background-position: 0 0;
  }
} */
</style>
