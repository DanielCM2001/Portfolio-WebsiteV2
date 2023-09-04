<template>
  <div class="min-h-screen flex justify-center items-center">
    <div class="flex justify-center items-center w-full flex-col md:flex-row">
      <div
        class="w-full lg:w-1/2 bg-slate-600 flex justify-center items-center flex-col"
      >
        <div class="w-1/2 space-y-10 bg-slate-700">
          <h1 class="text-5xl">Hi there! I'm Daniel</h1>
          <p class="text-2xl">
            A front-end Web Developer passionate about creating interactive
            applications and experiences on the web.
          </p>

          <div class="flex flex-row space-x-10">
            <button>1</button>
            <button>2</button>
          </div>
        </div>
      </div>
      <div class="w-full lg:w-1/2 flex justify-end">
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

<style lang="scss" scoped></style>
