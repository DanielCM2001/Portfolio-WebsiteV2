<template>
  <!--  <section
    class="relative flex items-center justify-center h-[100vh] text-white overflow-hidden SkyAnimated bg-[#03A9F4]"
  > -->

  <section
    class="flex items-center justify-center w-full h-[100vh] SkyAnimated text-white bg-[#03A9F4]"
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
      <!--   <img
        src="../../../assets/img/HouseBalloonsFirst.png"
        alt=""
        class="absolute h-[150px] bottom-[5%] right-20 z-0 sm:h-[250px] 2xl:h-[500px] balloon"
      /> -->
    </div>
    <!--   <img
      src="../../../assets/img/CloudOne.png"
      alt="Fixed Image"
      class="fixed bottom-0 left-0 opacity-0 cloudOne allClouds"
    />
    <img
      src="../../../assets/img/CloudTwo.png"
      alt="Fixed Image"
      class="fixed bottom-0 right-0 opacity-0 cloudTwo allClouds"
    /> -->
  </section>
</template>

<script>
export default {
  mounted() {
    /* ======================================================================== */
    /*   const tweenCloudOpacity = new TimelineLite();

    tweenCloudOpacity.add(
      TweenLite.to(".allClouds", 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    );

    const controllerCloudOpacity = new ScrollMagic.Controller();

    const sceneCloudOpacity = new ScrollMagic.Scene({
      triggerElement: ".SkyAnimated",
      duration: 400,
      triggerHook: 1,
    })
      .setTween(tweenCloudOpacity)
      .addTo(controllerCloudOpacity);

    const tweenClouds = new TimelineLite();

    tweenClouds.add(
      TweenLite.to([".cloudOne", ".cloudTwo"], 1, {
        transform: "translate(-10%, 50%) translate3d(0px, 0px, 0px) scale(1.5)",
        ease: Linear.easeNone,
      })
    );

    const controllerCloudPath = new ScrollMagic.Controller();

    const sceneCloud = new ScrollMagic.Scene({
      triggerElement: ".SkyAnimated",
      duration: "100%",
      triggerHook: 0,
    })
      .setTween(tweenClouds)
      .addTo(controllerCloudPath); */
    /* ======================================================================== */
    /*  const BalloonPath = {
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
      .addTo(controllerBalloon); */
  },
};
</script>

<style scoped></style>
