<template>
  <!-- ================================== -->
  <!--   <div class="h-[25vh] skycontainer"></div> -->
  <!-- ================================== -->

  <section
    class="relative flex flex-col items-end justify-center text-white animation skycontainer"
  >
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

    <!-- Clouds come here -->
    <!--  <img
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
  <!-- ================================== -->
  <div class="gap h-[100vh]">
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
  </div>
  <!-- ================================== -->
</template>

<script>
export default {
  mounted() {
    /*  const tweenSkyBackground = new TimelineLite();

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
      .addTo(this.controller); */

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
      TweenLite.to(".allClouds", 0, {
        opacity: 0,
        ease: Linear.easeNone,
      })
    );

    tweenCloudsPlaneOpacity.add(
      TweenLite.to(".allClouds", 1, {
        opacity: 1,
        ease: Linear.easeNone,
        /*    onUpdate: function () {
          if (document.querySelector(".allClouds").style.opacity == "1") {
            document.body.classList.add("skySpace-background");
          } else {
            document.body.classList.remove("skySpace-background");
          }
        }, */
        /*  onComplete: () => {
          document.body.classList.add("skySpace-background");
        },
        onReverseComplete: () => {
          document.body.classList.remove("skySpace-background");
        }, */

        onUpdate: function () {
          if (document.querySelector(".allClouds").style.opacity !== "0") {
            const darkspaceBackground = document.querySelector(
              ".darkspace-background"
            );
            darkspaceBackground.style.backgroundColor = "#0497d1";
          } else {
            const darkspaceBackground = document.querySelector(
              ".darkspace-background"
            );
            darkspaceBackground.style.backgroundColor = "#070707";
          }
        },
      })
    );

    const controllerlmap = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const sceneCloudPlaneOpacity = new ScrollMagic.Scene({
      triggerElement: ".skycontainer",
      duration: 200, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenCloudsPlaneOpacity)
      .addTo(controllerlmap);

    /* =========================================== */

    /*  const changetweenCloudsPlaneOpacity = new TimelineLite();

    changetweenCloudsPlaneOpacity.add(
      TweenLite.to(".allClouds", 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    );

    changetweenCloudsPlaneOpacity.add(
      TweenLite.to(".allClouds", 1, {
        opacity: 0,
        ease: Linear.easeNone,
        onUpdate: function () {
          if (document.querySelector(".allClouds").style.opacity != "1") {
            document.body.classList.remove("skySpace-background");
          } else {
            document.body.classList.add("skySpace-background");
          }
        },
      })
    );

    this.controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const changesceneCloudPlaneOpacity = new ScrollMagic.Scene({
      triggerElement: ".gap",
      duration: 200, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(changetweenCloudsPlaneOpacity)
      .addTo(this.controller); */

    /* const changetweenCloudsPlaneOpacity = new TimelineLite();

    changetweenCloudsPlaneOpacity.add(
      TweenLite.to(".allClouds", 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    );

    changetweenCloudsPlaneOpacity.add(
      TweenLite.to(".allClouds", 1, {
        opacity: 0,
        ease: Linear.easeNone,
      })
    );

    const controllerxd = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const changesceneCloudPlaneOpacity = new ScrollMagic.Scene({
      triggerElement: ".gap",
      duration: 200, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(changetweenCloudsPlaneOpacity)
      .addTo(controllerxd); */
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
