<!-- <template>
  <section class="h-[100vh] flex justify-center items-end spacecontainer">
    <h1>xd</h1>
  </section>
  <div class="h-[25vh]"></div>
  <section class="flex flex-col items-end justify-center skycontainer">
    <div class="h-[100vh] flex items-end justify-center w-full">
      <h1>First text</h1>
    </div>
    <div class="h-[100vh] flex items-end justify-center w-full">
      <h1>Second text</h1>
    </div>
  </section>
  <div class="gap h-[100vh]"></div>
</template>

<script>
export default {
  data() {
    return {
      controller: null,
    };
  },
  mounted() {
    const tween = new TimelineLite();

    tween.add(
      TweenLite.to({}, 1, {
        ease: Power1.easeInOut,
        onUpdate: () => {
          document.body.classList.add("darkspace-background");
        },
        onReverseComplete: () => {
          document.body.classList.remove("darkspace-background");
        },
      })
    );

    this.controller = new ScrollMagic.Controller();

    const spaceScene = new ScrollMagic.Scene({
      triggerElement: ".spacecontainer",
      duration: 100, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tween)
      .addTo(this.controller);

    const tweenlmao = new TimelineLite();

    tweenlmao.add(
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

    const spScene = new ScrollMagic.Scene({
      triggerElement: ".skycontainer",
      duration: 100, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenlmao)
      .addTo(this.controller);

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

    this.controller = new ScrollMagic.Controller();

    const newScene = new ScrollMagic.Scene({
      triggerElement: ".gap",
      duration: 100, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(newtween)
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
.animation {
  position: relative;
  height: 100vh;
  overflow: hidden;
}

.space {
  background-image: url("../../assets/img/NewSpaceBackground.png");
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  height: 100vh;
  width: 100%;
  animation: pump 4.5s infinite alternate;
}

@keyframes pump {
  0% {
    transform: translate3d(0);
  }
  100% {
    transform: translate3d(12px, -22px, -25px);
  }
}

.world-hide {
  transform: translateY(100%);
  transition: all 1s;
}

.world-show {
  transform: translateY(0);
}

.rocket-hide {
  transform: translateY(100%);
  transition: all 1s;
}

.rocket-show {
  transform: translateY(0);
}

.ovni-hide {
  transform: translateX(-100%);
  transition: all 1s;
}

.ovni-show {
  transform: translateX(0);
}

.moon-hide {
  transform: translateX(100%);
  transition: all 1s;
}

.moon-show {
  transform: translateX(0);
}
</style>
 -->
<!-- <section class="flex flex-col items-end justify-center text-white">
    <div class="h-[100vh] flex items-end justify-center w-full relative">
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px]">First phrase</p>
    </div>
    <div class="h-[100vh] flex items-end justify-center w-full">
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px]">Second phrase</p>
    </div>
  </section> -->
<!--  const tweenClouds = new TimelineLite(); tweenClouds.add(
TweenLite.to(".allClouds", 1, { opacity: 1, ease: Linear.easeNone, }) );
tweenClouds.add( TweenLite.to(".cloudOne", 1, { transform: "translate(-50%, 10%)
translate3d(0px, 0px, 0px) scale(1.5)", ease: Linear.easeNone, }) );
tweenClouds.add( TweenLite.to(".cloudTwo", 1, { transform: "translate(50%, 10%)
translate3d(0px, 0px, 0px) scale(1.5)", ease: Linear.easeNone, }) );
this.controller = new ScrollMagic.Controller(); // Create a ScrollMagic scene
const sceneCloud = new ScrollMagic.Scene({ triggerElement: ".skycontainer",
duration: "100%", // Adjust the duration as needed triggerHook: 0, })
.setTween(tweenClouds) .addTo(this.controller);  -->
<template>
  <section
    class="h-[100vh] relative flex flex-col items-center justify-center overflow-hidden spacecontainer"
  >
    <div class="bottom-0 opacity-0 space"></div>

    <div
      class="absolute bottom-0 left-0 z-30 flex items-center justify-center min-w-full min-h-full world-wrapper animatedWorld"
    >
      <img
        src="../../assets/img/WorldX4.png"
        alt=""
        class="absolute h-[200px] bottom-[0%] z-10 sm:h-[300px] 2xl:h-[400px] world-world world-hide"
      />
    </div>

    <h1
      class="text-center text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[40px] lg:text-[70px] 2xl:text-[80px] z-10"
    >
      I enjoy creating things that live
      <br class="hidden lg:flex" />
      on the internet...
    </h1>
  </section>

  <!-- ================================== -->
  <div class="h-[25vh]"></div>
  <!-- ================================== -->

  <section
    class="flex flex-col items-end justify-center text-white skycontainer"
  >
    <!-- First Phrase comes here -->
    <div
      class="h-[100vh] flex items-end justify-center w-full relative animation overflow-hidden"
    >
      <img
        src="../../assets/img/Plane.png"
        alt=""
        class="plane top-[50%] left-0 absolute h-[100px] lg:h-[150px] 2xl:h-[200px]"
      />
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px]">First phrase</p>
    </div>

    <!-- Second Phrase comes here -->
    <div class="h-[100vh] flex items-end justify-center w-full relative">
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px]">Second phrase</p>
    </div>

    <!-- Clouds come here -->
    <img
      src="../../assets/img/CloudOne.png"
      alt="Fixed Image"
      class="fixed bottom-0 left-0 opacity-0 cloudOne allClouds"
    />
    <img
      src="../../assets/img/CloudTwo.png"
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
    const tween = new TimelineLite();

    tween.add(
      TweenLite.to({}, 1, {
        ease: Power1.easeInOut,
        onUpdate: () => {
          document.body.classList.add("darkspace-background");
        },
        onReverseComplete: () => {
          document.body.classList.remove("darkspace-background");
        },
      })
    );

    this.controller = new ScrollMagic.Controller();

    const spaceScene = new ScrollMagic.Scene({
      triggerElement: ".spacecontainer",
      duration: 100, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tween)
      .addTo(this.controller);

    const tweenWorld = new TimelineLite();

    tweenWorld.add(
      TweenLite.to(".space", 0, {
        opacity: 0,
        ease: Linear.easeNone,
      })
    );

    tweenWorld.add(
      TweenLite.to(".space", 1, {
        opacity: 1,
        ease: Linear.easeNone,
        onUpdate: function () {
          if (document.querySelector(".space").style.opacity <= "0.4") {
            document
              .querySelector(".world-world")
              .classList.remove("world-show");
          } else {
            document.querySelector(".world-world").classList.add("world-show");
          }
        },
      })
    );

    tweenWorld.add(
      TweenLite.to(".world-wrapper", 1, {
        scale: 5,
        ease: Linear.easeNone,
      })
    );

    this.controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const sceneWorld = new ScrollMagic.Scene({
      triggerElement: ".spacecontainer",
      duration: 1000, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenWorld)
      .setPin(".spacecontainer")
      .addTo(this.controller);

    /* ================================================================ */

    const tweenSkyBG = new TimelineLite();

    tweenSkyBG.add(
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
    const skyBGScene = new ScrollMagic.Scene({
      triggerElement: ".skycontainer",
      duration: 100, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenSkyBG)
      .addTo(this.controller);

    /* ======================================================================== */

    const tweenClouds = new TimelineLite();

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
      .addTo(this.controller);

    /*====================== Space Section ======================*/

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

    /* ======================================================================== */

    /*     const newtween = new TimelineLite();

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
        ease: Linear.easeNone,
      })
    );

    this.controller = new ScrollMagic.Controller();

    const newScene = new ScrollMagic.Scene({
      triggerElement: ".gap",
      duration: 400, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(newtween)
      .setPin(".gap")
      .addTo(this.controller); */
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

.space {
  background-image: url("../../assets/img/NewSpaceBackground.png");
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  height: 100vh;
  width: 100%;
  animation: pump 4.5s infinite alternate;
}

.spacestars {
  background-image: url("../../assets/img/StarsBackground.png");
  /*  background-size: cover;
  background-repeat: no-repeat;
  position: absolute; */
  height: 100%;
  width: 100%;
}

@keyframes pump {
  0% {
    transform: translate3d(0);
  }
  100% {
    transform: translate3d(12px, -22px, -25px);
  }
}

.world-hide {
  transform: translateY(100%);
  transition: all 1s;
}

.world-show {
  transform: translateY(0);
}
</style>
