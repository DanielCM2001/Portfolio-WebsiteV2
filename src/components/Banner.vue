<template>
  <div class="flex items-center justify-center min-h-screen">
    <div class="flex flex-col items-center justify-center w-full md:flex-row">
      <div class="flex flex-col items-center justify-center w-full lg:w-1/2">
        <div class="w-full space-y-10 lg:w-1/2">
          <h1 class="text-5xl">Hi there! I'm Daniel</h1>
          <p class="text-2xl">
            A front-end Web Developer passionate about creating interactive
            applications and experiences on the web.
          </p>

          <div class="flex flex-row space-x-10 text-lg">
            <button class="px-8 py-3 primaryButtons">LinkedIn</button>
            <button class="px-5 py-3 primaryButtons">Icon</button>
            <button class="px-5 py-3 primaryButtons">Icon</button>
          </div>
        </div>
      </div>
      <div class="flex justify-end w-full lg:w-1/2">
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
</style>
