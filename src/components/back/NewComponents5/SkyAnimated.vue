<template>
  <section
    class="flex items-center justify-center w-full h-[100vh] relative SkyAnimated text-white bg-[#03A9F4]"
  >
    <div class="z-10 flex flex-col mx-4">
      <p class="text-[20px] lg:text-[25px] 2xl:text-[35px] opacity-85">
        My interest in Web Development started back in 2017
      </p>
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px]">
        When I decided to try making a <br class="hidden lg:flex" />
        website for a school project
      </p>
      <p class="text-[20px] lg:text-[25px] 2xl:text-[35px] opacity-85">
        Turns out making a school project taught me a lot about web
      </p>
      <img
        src="../../../assets/img/HouseBalloonsFirst.png"
        alt=""
        class="absolute h-[150px] bottom-[5%] right-20 z-0 sm:h-[250px] 2xl:h-[500px] balloon"
      />
    </div>
    <!--   <img
      src="../../../assets/img/CloudOne.png"
      alt="Fixed Image"
      class="fixed bottom-0 left-0 z-10 opacity-0 cloudOne allClouds"
      style="transform: translate(0%, 60%) translate3d(0px, 0px, 0px) scale(1)"
    />
    <img
      src="../../../assets/img/CloudTwo.png"
      alt="Fixed Image"
      class="fixed bottom-0 right-0 z-10 opacity-0 cloudTwo allClouds"
      style="transform: translate(0%, 60%) translate3d(0px, 0px, 0px) scale(1)"
    /> -->
  </section>
</template>

<script>
export default {
  mounted() {
    /* ======================================================================== */
    const BalloonPath = {
      curviness: 1.25,
      autoRotate: false,
      values: [
        {
          x: 0,
          y: -100,
        },
        {
          x: 0,
          y: -200,
        },
        {
          x: -100,
          y: -300,
        },
        {
          x: -200,
          y: -400,
        },
      ],
    };

    const tweenBalloon = new TimelineLite();

    tweenBalloon.add(
      TweenLite.to(".balloon", 1, {
        bezier: BalloonPath,
        ease: Linear.easeInOut,
      })
    );

    const controllerBalloon = new ScrollMagic.Controller();

    const sceneBalloon = new ScrollMagic.Scene({
      triggerElement: ".SkyAnimated",
      duration: 1000,
      triggerHook: 0.4,
    })
      .setTween(tweenBalloon)
      .addTo(controllerBalloon);
  },
};
</script>

<style scoped></style>
