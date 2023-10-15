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
  <div class="flex items-center justify-center w-full bg-gray-600">
    <div
      class="w-full xs:w-9/12 md:w-full md:mx-[15vw] static-container justify-center text-center items-center flex flex-col bg-gray-800"
    >
      <div class="py-10">
        <p class="text-2xl">What I did?</p>
        <p class="text-3xl glowLabel">Portfolio</p>
        <p class="text-4xl">Some of my projects...</p>
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
.box {
  border-radius: 40px;
  background: #151417;
  box-shadow:
    0px 3px 3px 0px #8c5dc9 inset,
    0px 4px 40px 0px #c940eb;
}

/* class="relative p-[calc(50vh-3.5rem)] m-0 lg:m-0 xl:m-25vw min-h-screen perspective-900 perspective-origin-center lg:perspective-origin-50-top"> */
.static-container {
  padding: calc(50vh - 3.5rem) 0 0;
  min-height: 100vh;
  perspective: 900px;
  perspective-origin: 50% 50vh;
}
.glowLabel {
  color: #c940eb;
  text-shadow: 0px 4px 50px #c940eb;
}
</style>
