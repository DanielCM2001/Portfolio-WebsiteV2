<template>
  <!-- ================================== -->
  <div class="h-[25vh] skycontainer"></div>
  <!-- ================================== -->

  <section class="flex flex-col items-end justify-center text-white animation">
    <!-- First Phrase comes here -->
    <div
      class="h-[100vh] flex items-end justify-center w-full relative overflow-hidden"
    >
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px]">First phrase</p>
    </div>

    <!-- Second Phrase comes here -->
    <div class="h-[100vh] flex items-end justify-center w-full relative">
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px]">Second phrase</p>
    </div>

    <img
      src="../../../assets/img/Plane.png"
      alt=""
      class="plane top-[40%] left-0 fixed h-[100px] lg:h-[150px] 2xl:h-[200px] opacity-0"
    />
    <!-- Clouds come here -->
    <img
      src="../../../assets/img/CloudOne.png"
      alt="Fixed Image"
      class="fixed bottom-0 left-0 opacity-0 cloudOne allClouds"
    />
    <img
      src="../../../assets/img/CloudTwo.png"
      alt="Fixed Image"
      class="fixed bottom-0 right-0 opacity-0 cloudTwo allClouds"
    />
  </section>
  <!-- ================================== -->
  <div class="gap h-[100vh]"></div>
  <!-- ================================== -->
</template>

<script>
export default {
  data() {
    return {
      controller: null,
    };
  },
  mounted() {
    const tweenSkyBackground = new TimelineLite();

    tweenSkyBackground.add(
      TweenLite.to({}, 1, {
        ease: Power1.easeInOut,
        onUpdate: () => {
          document.body.classList.add("skySpace-background");
        },
        onReverseComplete: () => {
          document.body.classList.remove("skySpace-background");
        },
      })
    );

    this.controller = new ScrollMagic.Controller();
    const skyBackgroundScene = new ScrollMagic.Scene({
      triggerElement: ".skycontainer",
      duration: 100, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenSkyBackground)
      .addTo(this.controller);

    /* ======================================================================== */

    /* const tweenClouds = new TimelineLite();

    tweenClouds.add(
      TweenLite.to(".allClouds", 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    );

    tweenClouds.add(
      TweenLite.to([".cloudOne", ".cloudTwo"], 1, {
        transform: "translate(-10%, 50%) translate3d(0px, 0px, 0px) scale(1.5)",
        ease: Linear.easeNone,
      })
    );

    this.controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const sceneCloud = new ScrollMagic.Scene({
      triggerElement: ".skycontainer",
      duration: "100%", // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenClouds)
      .addTo(this.controller); */

    /*============================================*/

    /* const PlaneflightPath = {
      curviness: 1.25,
      autoRotate: true,
      values: [
        {
          x: window.innerWidth,
          y: 0,
        },
      ],
    };

    const tweenPlane = new TimelineLite();

    tweenPlane.add(
      TweenLite.to(".plane", 1, {
        bezier: PlaneflightPath,
        ease: Power1.easeInOut,
      })
    );

    const controllerPlane = new ScrollMagic.Controller();

    const scenePlane = new ScrollMagic.Scene({
      triggerElement: ".animation",
      duration: 1000,
      triggerHook: 0,
    })
      .setTween(tweenPlane)
      .addTo(controllerPlane); */

    /* ======================================================================== */
    const tweenCloudsPlaneOpacity = new TimelineLite();

    tweenCloudsPlaneOpacity.add(
      TweenLite.to([".allClouds", ".plane"], 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    );

    this.controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const sceneCloudPlaneOpacity = new ScrollMagic.Scene({
      triggerElement: ".skycontainer",
      duration: 200, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenCloudsPlaneOpacity)
      .addTo(this.controller);

    /* =========================================== */
    const PlaneflightPath = {
      curviness: 1.25,
      autoRotate: true,
      values: [
        {
          x: window.innerWidth,
          y: 0,
        },
      ],
    };

    const tweenPlane = new TimelineLite();

    tweenPlane.add(
      TweenLite.to(".plane", 1, {
        bezier: PlaneflightPath,
        ease: Power1.easeInOut,
      })
    );

    const controllerPlane = new ScrollMagic.Controller();

    const scenePlane = new ScrollMagic.Scene({
      triggerElement: ".animation",
      duration: 1000,
      triggerHook: 0,
    })
      .setTween(tweenPlane)
      .addTo(controllerPlane);
  },
  beforeDestroy() {
    if (this.controller) {
      this.controller.destroy(true);
    }
  },
};
</script>

<style scoped>
/* .animation {
    position: relative;
    height: 100vh;
    overflow: hidden;
  } */
</style>
