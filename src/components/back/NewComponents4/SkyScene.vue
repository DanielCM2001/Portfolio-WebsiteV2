<template>
  <!-- ================================== -->
  <div
    class="h-[90vh] planecontainer skycontainer relative flex items-end justify-center"
  >
    <!-- <h1
      class="text-center text-white text-[40px] lg:text-[70px] 2xl:text-[80px]"
    >
      &lt;Wrapper&gt;
    </h1> -->

    <!-- <h1
      class="text-[#9d32b7] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[40px] lg:text-[3rem] 2xl:text-[4rem] font-semibold z-10"
    >
      3D models, matte painting and
      <br class="hidden lg:flex" />
      advertisements
    </h1> -->

    <div class="z-30 flex flex-col">
      <p class="text-[20px] lg:text-[25px] 2xl:text-[30px] opacity-85">
        My interest in Web Development started back in 2017
      </p>
      <p
        class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[40px] lg:text-[3rem] 2xl:text-[4rem] font-semibold z-10"
      >
        When I decided to try making a <br class="hidden lg:flex" />
        website for a school project
      </p>
      <p class="text-[20px] lg:text-[25px] 2xl:text-[30px] opacity-85">
        Turns out making a school project taught me a lot about web
      </p>
    </div>

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
    <!--  <div
      class="h-[100vh] flex items-end justify-center w-full relative overflow-hidden"
    >
      <p class="text-[30px] lg:text-[45px] 2xl:text-[60px] z-30">
        Always striving to create the <br class="hidden lg:flex" />
        unexpected by challenging the now
      </p>
    </div> -->

    <!-- Second Phrase comes here -->
    <!--   <div class="h-[100vh] flex items-end justify-center w-full relative">
      <div class="z-30 flex flex-col">
        <p class="text-[20px] lg:text-[25px] 2xl:text-[30px] opacity-85">
          My interest in Web Development started back in 2017
        </p>
        <p
          class="text-[#9d32b7] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[40px] lg:text-[3rem] 2xl:text-[4rem] font-semibold z-10"
        >
          When I decided to try making a <br class="hidden lg:flex" />
          website for a school project
        </p>
        <p class="text-[20px] lg:text-[25px] 2xl:text-[30px] opacity-85">
          Turns out making a school project taught me a lot about web
        </p>
      </div>
    </div> -->

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

  <div
    class="z-40 flex items-stretch justify-center w-full min-h-screen text-white designerCoder"
  >
    <div
      class="flex flex-col items-end justify-center w-full pl-5 pr-5 max-w-screen-2xl md:flex-row md:space-x-10"
    >
      <!-- Left Side -->
      <div class="flex flex-col items-center justify-center w-full text-center">
        <p class="py-5 text-[70px] lg:text-[90px] 2xl:text-[120px] hide">
          Designer
        </p>

        <p class="text-xl lg:text-2xl 2xl:text-3xl hide">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et dolore
          magna aliqua. Ut enim ad minim veniam, qu
        </p>
      </div>

      <!-- Right Side -->
      <div class="flex flex-col items-center justify-center w-full text-center">
        <p class="py-5 text-[70px] lg:text-[90px] 2xl:text-[120px] hide">
          Coder++
        </p>

        <p class="text-xl lg:text-2xl 2xl:text-3xl hide">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et dolore
          magna aliqua. Ut enim ad minim veniam, qu
        </p>
      </div>
    </div>
  </div>
  <div class="h-[20vh]"></div>

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
      TweenLite.to(".skycontainer", 1, {
        ease: Power1.easeInOut,
        onComplete: () => {
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
      triggerHook: 0.2,
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

    /* ENDING */

    const newtween = new TimelineLite();
    newtween.add(
      TweenLite.to({}, 1, {
        ease: Power1.easeInOut,
        onUpdate: () => {
          document.body.classList.remove("darkspace-background");
          document.body.classList.remove("skySpace-background");
        },
        onReverseComplete: () => {
          document.body.classList.add("skySpace-background");
          document.body.classList.add("darkspace-background");
        },
      })
    );

    newtween.add(
      TweenLite.to(".allClouds", 1, {
        opacity: 0,
        ease: Power1.easeInOut,
      })
    );

    this.controller = new ScrollMagic.Controller();

    const newScene = new ScrollMagic.Scene({
      triggerElement: ".gap",
      duration: 600, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(newtween)
      .setPin(".gap")
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
