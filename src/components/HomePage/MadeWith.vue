<!-- <template>
  <div
    class="flex flex-col items-center justify-center w-full min-h-[50vh] bg-gray-700"
  >
    <div class="absolute left-0 flex items-center justify-start mt-20">
      <img
        src="../assets/img/BannerRectangle2.png"
        alt="Banner image"
        class="w-full max-w-md"
      />

      <img
        src="../assets/img/Avatar2Changed.png"
        alt="Banner image"
        class="w-full max-w-[350px] absolute"
      />
    </div>

    <div class="flex flex-col w-1/4 space-y-5 bg-gray-600">
      <div>
        <h1
          class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[30px]"
        >
          //Made with
        </h1>
      </div>
      <div class="flex flex-row">
        <div class="flex flex-col w-1/3 space-y-5 bg-gray-500">
          <h1>(){&lt;/&gt;}</h1>

          <div class="space-y-0">
            <p>Javascript,</p>
            <p>CSS, HTML,</p>
            <P>Vue,</P>
            <P>Figma,</P>
            <P>GSAP</P>
          </div>
        </div>
        <div class="flex flex-col w-1/3 space-y-5 bg-gray-500">
          <h1>~</h1>

          <div>
            <p>+10 cups of cappuccino</p>
            <p>+4 mixed cheese and ham toast</p>
          </div>
        </div>
        <div class="flex flex-col w-1/3 space-y-5 bg-gray-500">
          <h1>🎵</h1>

          <div>
            <p>MUSIC 1</p>
            <p>MUSIC 2</p>
            <p>MUSIC 3</p>
            <p>MUSIC 4</p>
          </div>
        </div>
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

<style lang="scss" scoped></style> -->

<!-- <template>
  <div class="relative flex items-center justify-center mb-20">
    <img
      src="../assets/img/Avatar2Changed.png"
      alt=""
      class="absolute h-[350px] top-auto left-0"
    />
    <div
      class="w-full xs:w-9/12 lg:w-full lg:mx-[30vw] static-container pt-[20vh] mx-5 space-y-5"
    >
      <h1
        class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[30px]"
      >
        //Made with
      </h1>

      <div
        class="grid gap-y-[1rem] md:grid-flow-col md:grid-cols-3 md:gap-x-[4rem] xl:gap-x-[4rem]"
      >
        <ul class="space-y-5">
          <h1>(){&lt;/&gt;}</h1>
          <li class="space-y-0">
            <p>Javascript,</p>
            <p>CSS, HTML,</p>
            <P>Vue,</P>
            <P>Figma,</P>
            <P>GSAP</P>
          </li>
        </ul>

        <ul class="space-y-5">
          <h1>~</h1>
          <li class="space-y-0">
            <p>+10 cups of cappuccino,</p>
            <p>+4 mixed cheese and ham toasts</p>
          </li>
        </ul>

        <ul class="space-y-5">
          <h1>🎵</h1>
          <li class="space-y-0">
            <p>Music 1</p>
            <p>Music 2</p>
            <p>Music 3</p>
            <p>Music 4</p>
          </li>
        </ul>
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
.static-container {
  padding: calc(50vh - 3.5rem) 0 0;
  min-height: 100vh;
  perspective: 900px;
  perspective-origin: 50% 50vh;
}
</style> -->
<!-- ================================================================== -->
<template>
  <div
    class="flex flex-col items-center justify-center w-full py-10 sm:flex-row"
  >
    <div
      class="absolute left-0 flex items-center justify-start w-full -mt-20 opacity-10 xl:opacity-100"
    >
      <!-- <img
        src="../../assets/img/BannerRectangle2.png"
        alt="Banner image"
        class="w-full max-w-xs xs:max-w-sm lg:max-w-md"
      /> -->

      <img
        src="../../assets/img/Avatar2Changed.png"
        alt="Banner image"
        class="w-full max-w-[250px] xs:max-w-[300px] lg:max-w-[320px] absolute drop-shadow-[0_4px_10px_rgba(195,2,58,1)]"
      />
    </div>
    <!-- drop-shadow-[0_35px_35px_rgba(0,0,0,0.25)] -->

    <!-- [shadow:0_4px_50px_rgba(195,2,58,1)] -->
    <div
      class="w-full xs:w-9/12 lg:w-full lg:mx-[25vw] xl:mx-[30vw] px-5 space-y-5 static-container flex flex-col"
    >
      <h1
        class="text-[#C3023A] [text-shadow:0_4px_50px_rgba(195,2,58,1)] text-[30px]"
      >
        //Made with
      </h1>

      <div
        class="grid gap-y-[1rem] sm:grid-flow-col sm:grid-cols-3 sm:gap-x-[4rem] xl:gap-x-[2rem]"
      >
        <ul class="space-y-5 text-xl">
          <h1>(){&lt;/&gt;}</h1>
          <li class="space-y-0 text-lg">
            <p>Javascript,</p>
            <p>CSS, HTML,</p>
            <P>Vue,</P>
            <P>Figma,</P>
            <P>GSAP</P>
          </li>
        </ul>

        <ul class="space-y-5 text-xl">
          <h1>~</h1>
          <li class="space-y-0 text-lg">
            <p>+10 cups of cappuccino,</p>
            <p>+4 mixed cheese and ham toasts</p>
          </li>
        </ul>

        <ul class="space-y-5 text-xl">
          <h1>🎵</h1>
          <li class="space-y-0 text-lg">
            <p>Music 1</p>
            <p>Music 2</p>
            <p>Music 3</p>
            <p>Music 4</p>
          </li>
        </ul>
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
.static-container {
  /*  padding: calc(50vh - 3.5rem) 0 0; */
  min-height: 40vh;
  perspective: 900px;
  perspective-origin: 50% 50vh;
}
</style>
