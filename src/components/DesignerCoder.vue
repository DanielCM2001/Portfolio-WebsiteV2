<template>
  <div class="flex items-stretch justify-center w-full">
    <!-- ============================================= -->
    <div class="items-center justify-center hidden xs:flex xs:w-3/12 md:hidden">
      <div class="w-5 h-full separatorBar"></div>
    </div>
    <!-- ============================================= -->

    <div
      class="flex flex-col items-stretch justify-center w-full mt-20 mb-20 max-w-screen-2xl xs:w-9/12 md:flex-row"
    >
      <!-- Left Side -->
      <div
        class="flex flex-col items-center justify-center w-full md:w-2/5 md:ml-5 lg:ml-0 lg:w-2/5 2xl:w-1/5"
      >
        <p class="py-5 text-5xl DesignerText">Designer</p>

        <p class="text-lg">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et dolore
          magna aliqua. Ut enim ad minim veniam, qu
        </p>
      </div>

      <!-- Midle bar -->
      <div class="justify-center hidden -mb-[100px] md:flex md:w-1/5">
        <div class="w-5 h-full separatorBar"></div>
        <div
          class="absolute w-12 h-12 cursor-pointer separatorBox animate-glow"
        >
          <img
            src="../assets/img/IdeasIcon.png"
            class="object-contain w-full h-full px-2 py-2"
          />
        </div>
      </div>

      <!-- Right Side -->
      <div
        class="flex flex-col items-center justify-center w-full md:w-2/5 md:mr-5 lg:mr-0 lg:w-2/5 2xl:w-1/5"
      >
        <p class="py-5 text-5xl">Coder</p>

        <p class="text-lg">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et dolore
          magna aliqua. Ut enim ad minim veniam, qu
        </p>
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
.DesignerText {
  background: linear-gradient(
    91deg,
    #c940eb 6.27%,
    #9b8df3 43.87%,
    #8c5dc9 80.87%
  );
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.separatorBar {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}

.separatorBox {
  border-radius: 15px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
  animation: glow 1.5s infinite alternate; /* Glowing animation */
}

@keyframes glow {
  0% {
    box-shadow: 0 0 5px #c940eb; /* Initial glow effect */
    /*  width: 48px;
    height: 48px; */
  }
  100% {
    box-shadow: 0 0 30px #c940eb; /* Stronger glow effect */
    /*  width: 54px;
    height: 54px; */
  }
}
</style>
