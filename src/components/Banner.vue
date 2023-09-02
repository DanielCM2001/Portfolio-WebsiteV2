<template>
  <div class="min-h-screen flex justify-center items-center">
    <div
      class="flex justify-center items-center w-full flex-col md:flex-row space-y-20"
    >
      <div
        class="w-full lg:w-2/3 bg-slate-600 flex justify-center items-center"
      >
        <div class="w-1/3 space-y-10 bg-slate-700">
          <h1 class="text-5xl">Hi there! I'm Daniel</h1>
          <p class="text-2xl">
            A front-end Web Developer passionate about creating interactive
            applications and experiences on the web.
          </p>
        </div>
      </div>
      <div class="w-full lg:w-1/3 flex justify-end">
        <img
          src="../assets/img/BannerRectangle.png"
          alt="Banner image"
          class="w-full max-w-lg"
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

<style lang="scss" scoped></style>
