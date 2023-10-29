<template>
  <!-- ================================== -->
  <div class="h-[30vh] planecontainer skycontainer">
    <img
      src="../../../assets/img/Plane.png"
      alt=""
      class="plane -left-[20%] top-[20%] fixed h-[100px] lg:h-[150px] 2xl:h-[200px] opacity-0"
    />
  </div>
  <!-- ================================== -->

  <section
    class="relative flex flex-col items-end justify-center overflow-hidden text-white animation"
  >
    <!-- First Phrase comes here -->
    <div
      class="h-[100vh] flex items-end justify-center w-full relative overflow-hidden"
    >
      <p class="text-[30px] lg:text-[45px] 2xl:text-[60px] z-30">
        Always striving to create the <br class="hidden lg:flex" />
        unexpected by challenging the now
      </p>
    </div>

    <!-- Second Phrase comes here -->
    <div class="h-[100vh] flex items-end justify-center w-full relative">
      <div class="z-30 flex flex-col">
        <p class="text-[20px] lg:text-[25px] 2xl:text-[35px] opacity-85">
          My interest in Web Development started back in 2017
        </p>
        <p class="text-[30px] lg:text-[45px] 2xl:text-[60px]">
          When I decided to try making a <br class="hidden lg:flex" />
          website for a school project
        </p>
        <p class="text-[20px] lg:text-[25px] 2xl:text-[35px] opacity-85">
          Turns out making a school project taught me a lot about web
        </p>
        <img
          src="../../assets/img/HouseBalloonsFirst.png"
          alt=""
          class="absolute h-[150px] bottom-[5%] right-20 z-0 sm:h-[250px] 2xl:h-[500px] balloon"
        />
      </div>
    </div>

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
    /* ======================================================================== */
    /* Change Sky Background to Blue */
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
    /* Change Plane Opacity */

    const tweenPlaneOpacity = new TimelineLite();

    tweenPlaneOpacity.add(
      TweenLite.to(".plane", 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    );

    this.controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const scenePlaneOpacity = new ScrollMagic.Scene({
      triggerElement: ".skycontainer",
      duration: 200, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenPlaneOpacity)
      .addTo(this.controller);

    /* ======================================================================== */
    /* Change Cloud Opacity */
    const tweenCloudOpacity = new TimelineLite();

    tweenCloudOpacity.add(
      TweenLite.to(".allClouds", 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    );

    this.controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const sceneCloudOpacity = new ScrollMagic.Scene({
      triggerElement: ".skycontainer",
      duration: 400, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenCloudOpacity)
      .addTo(this.controller);

    /* =========================================== */
    const PlaneflightPath = {
      curviness: 1.25,
      autoRotate: true,
      values: [
        {
          x: window.innerWidth * 2,
          y: 0,
        },
      ],
    };

    const tweenPlane = new TimelineLite();

    tweenPlane.add(
      TweenLite.to([".plane", "allClouds"], 1, {
        bezier: PlaneflightPath,
        ease: Power1.easeInOut,
      })
    );

    const controllerPlane = new ScrollMagic.Controller();

    const scenePlane = new ScrollMagic.Scene({
      triggerElement: ".planecontainer",
      duration: 1000,
      triggerHook: 0,
    })
      .setTween(tweenPlane)
      .addTo(controllerPlane);

    /* =========================================== */

    const tweenClouds = new TimelineLite();

    /*  tweenClouds.add(
      TweenLite.to(".allClouds", 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    ); */

    tweenClouds.add(
      TweenLite.to([".cloudOne", ".cloudTwo"], 1, {
        transform: "translate(-10%, 50%) translate3d(0px, 0px, 0px) scale(1.5)",
        ease: Linear.easeNone,
      })
    );

    this.controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const sceneCloud = new ScrollMagic.Scene({
      triggerElement: ".animation",
      duration: "200%", // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenClouds)
      .addTo(this.controller);
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
