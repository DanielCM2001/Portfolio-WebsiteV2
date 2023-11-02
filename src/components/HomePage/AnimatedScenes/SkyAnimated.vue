<template>
  <!-- ================================== -->
  <!--   <div class="h-[25vh] skycontainer"></div> -->

  <section
    class="relative flex flex-col items-center justify-center text-white skycontainer"
  >
    <!--  First Phrase comes here
    <div
      class="h-[100vh] flex items-center justify-center w-full relative overflow-hidden bg-[#03a9f4]"
    >
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px]">First phrase</p>
    </div>

    Second Phrase comes here
    <div
      class="h-[100vh] flex items-center justify-center w-full relative bg-gradient-to-b from-[#03a9f4] from-0% to-[#03a9f4] to-80%"
    >
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px]">Second phrase</p>
    </div> -->

    <!-- First Phrase comes here -->
    <div
      class="h-[100vh] flex items-center justify-center w-full relative overflow-hidden bg-[#03a9f4]"
    >
      <div class="z-30 flex flex-col mx-4">
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
      </div>
    </div>

    <!--  Second Phrase comes here -->
    <div
      class="h-[100vh] flex items-center justify-center w-full relative bg-gradient-to-b from-[#03a9f4] from-0% to-[#03a9f4] to-80%"
    >
      <div
        class="z-30 flex flex-col items-stretch justify-center w-full pl-5 pr-5 max-w-screen-2xl md:flex-row md:space-x-10"
      >
        <!-- Left Side -->
        <div
          class="flex flex-col items-center justify-center w-full text-center"
        >
          <p class="text-[70px] lg:text-[90px] 2xl:text-[120px] hide">
            Designer
          </p>

          <p class="text-xl lg:text-2xl 2xl:text-3xl hide">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et
            dolore magna aliqua. Ut enim ad minim veniam, qu
          </p>
        </div>

        <!-- Right Side -->
        <div
          class="flex flex-col items-center justify-center w-full text-center"
        >
          <p class="text-[70px] lg:text-[90px] 2xl:text-[120px] hide">
            Coder++
          </p>

          <p class="text-xl lg:text-2xl 2xl:text-3xl hide">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et
            dolore magna aliqua. Ut enim ad minim veniam, qu
          </p>
        </div>
      </div>
    </div>

    <!-- Animated Parts -->
    <img
      src="../../../assets/img/HouseBalloonsFirst.png"
      alt=""
      class="fixed bottom-[0%] right-20 h-[150px] sm:h-[250px] 2xl:h-[600px] balloon z-20 opacity-0"
    />

    <img
      src="../../../assets/img/CloudOne.png"
      alt="Fixed Image"
      class="fixed bottom-0 left-0 z-10 opacity-0 cloudOne"
      style="transform: translate(0%, 40%) translate3d(0px, 0px, 0px) scale(1)"
    />

    <img
      src="../../../assets/img/TestingGrass.png"
      alt="Fixed Image"
      class="fixed bottom-0 z-20 blur-[2px] opacity-0 grass"
      style="transform: translate(0%, 0%) translate3d(0px, 0px, 0px) scale(1)"
    />

    <img
      src="../../../assets/img/CloudTwo.png"
      alt="Fixed Image"
      class="fixed bottom-0 right-0 z-10 opacity-0 cloudTwo"
      style="transform: translate(0%, 70%) translate3d(0px, 0px, 0px) scale(1)"
    />
  </section>
  <!-- ================================== -->
  <div
    class="gap h-[100vh] bg-gradient-to-b from-[#03a9f4] from-0% to-[#66B7DC] to-80%"
  ></div>
</template>

<script>
export default {
  mounted() {
    const tweenCloudsPlaneOpacity = new TimelineLite();

    tweenCloudsPlaneOpacity.add(
      TweenLite.to([".cloudOne", ".cloudTwo", ".balloon", ".grass"], 0, {
        opacity: 0,
        ease: Linear.easeNone,
      })
    );

    tweenCloudsPlaneOpacity.add(
      TweenLite.to([".cloudOne", ".cloudTwo", ".balloon", ".grass"], 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    );

    const controllerlmap = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const sceneCloudPlaneOpacity = new ScrollMagic.Scene({
      triggerElement: ".skycontainer",
      duration: 200, // Adjust the duration as needed
      triggerHook: 0.5,
    })
      .setTween(tweenCloudsPlaneOpacity)
      .addTo(controllerlmap);

    /* ))))))))))))))))))))))))))))))))))))))))))))))) */

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
        {
          x: -200,
          y: -window.innerHeight,
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
      triggerElement: ".skycontainer",
      duration: "300%",
      triggerHook: 0.4,
    })
      .setTween(tweenBalloon)
      .addTo(controllerBalloon);
    /* ============================================ */

    const tweenClouds = new TimelineLite({ stagger: 0.1 });

    /*  tweenClouds.add(
      TweenLite.to([".cloudOne", ".cloudTwo", ".grass"], 1, {
        transform: "translate(0%, 0%) translate3d(0px, 0px, 0px) scale(1.5)",
        ease: Linear.easeNone,
      })
    ); */

    /*  tweenClouds.to([".cloudOne", ".cloudTwo"], 1, {
      transform: "translate(0%, 0%) translate3d(0px, 0px, 0px) scale(1.5)",
    });
    tweenClouds.to(
      ".grass",
      1,
      { transform: "translate(0%, 10%) translate3d(0px, 0px, 0px) scale(2)" },
      "0"
    ); */

    /*  gsap.registerPlugin(ScrollTrigger);

    ScrollTrigger.create({
      trigger: ".holdMe",
      animation: gsap.fromTo(".resizeMe", { scale: 1 }, { scale: 10 }),
      pin: true,
      start: "center center",
      end: "bottom top",
      scrub: 1, // I like the 1 sec delay, set to true for exact anime on scroll
      //markers: true,
    }); */

    tweenClouds.to([".cloudOne", ".cloudTwo"], 1, {
      transform: "translate(0%, 0%) translate3d(0px, 0px, 0px) scale(1.5)",
    });

    tweenClouds.to(
      ".grass",
      1,
      { transform: "translate(0%, 10%) translate3d(0px, 0px, 0px) scale(2)" },
      "0"
    );

    const controllerCloudPath = new ScrollMagic.Controller();

    const sceneCloud = new ScrollMagic.Scene({
      triggerElement: ".skycontainer",
      duration: "300%",
      triggerHook: 0.5,
    })
      .setTween(tweenClouds)
      .addTo(controllerCloudPath);

    /* ======================================= */
    const changetweenCloudsPlaneOpacity = new TimelineLite();

    changetweenCloudsPlaneOpacity.add(
      TweenLite.to([".cloudOne", ".cloudTwo", ".balloon", ".grass"], 1, {
        opacity: 0,
        ease: Linear.easeNone,
      })
    );

    const controllerxd = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const changesceneCloudPlaneOpacity = new ScrollMagic.Scene({
      triggerElement: ".gap",
      duration: "100%", // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(changetweenCloudsPlaneOpacity)
      .setPin(".gap")
      .addTo(controllerxd);
  },
};
</script>

<style scoped></style>
