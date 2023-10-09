<template>
  <div class="flex items-stretch justify-center w-full">
    <!-- ============================================= -->
    <div class="justify-center hidden xs:flex xs:w-3/12 md:hidden">
      <div class="w-5 h-full separatorBar"></div>
      <div class="absolute w-12 h-12 cursor-pointer separatorBox animate-glow">
        <img
          src="../assets/img/IdeasIcon.png"
          class="object-contain w-full h-full px-2 py-2"
        />
      </div>
    </div>
    <!-- ============================================= -->

    <!--  <div
      class="flex flex-col items-stretch justify-center w-full my-20 max-w-screen-2xl xs:w-9/12 md:flex-row"
    >
      <div class="justify-center hidden -my-[100px] md:flex md:w-1/5">
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
    </div> -->

    <!--   <p class="text-2xl">What I did?</p>
        <p class="text-3xl glowLabel">Portfolio</p>
        <p class="text-4xl">Some of my projects...</p> -->

    <div
      class="flex flex-col items-stretch justify-center w-full max-w-screen-2xl xs:w-9/12"
    >
      <div class="flex flex-col justify-center text-center items-center">
        <div class="hidden md:flex md:w-1/5 md:justify-center -mt-[20px]">
          <div class="w-5 h-64 separatorBar"></div>
          <div
            class="absolute w-12 h-12 cursor-pointer separatorBox animate-glow mt-52"
          >
            <img
              src="../assets/img/IdeasIcon.png"
              class="object-contain w-full h-full px-2 py-2"
            />
          </div>
        </div>
        <div class="py-10">
          <p class="text-2xl">What I did?</p>
          <p class="text-3xl glowLabel">Portfolio</p>
          <p class="text-4xl">Some of my projects...</p>
        </div>
      </div>

      <div class="bg-gray-800">Portfolio here</div>
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
