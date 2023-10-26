<template>
  <section class="h-[80vh] flex justify-center items-center newspacecontainer">
    <h1
      class="animatedText text-center text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[40px] lg:text-[60px] 2xl:text-[70px] z-10"
    >
      I enjoy creating things that live
      <br class="hidden lg:flex" />
      on the internet...
      <br />
    </h1>
  </section>

  <section
    class="relative flex flex-col items-center justify-center min-h-screen overflow-hidden spacecontainer"
  >
    <div class="bottom-0 opacity-0 space"></div>

    <!--   <div
      class="absolute bottom-0 left-0 z-30 flex items-center justify-center min-w-full min-h-full rocket-wrapper"
    >
      <img
        src="../../assets/img/Rocket.png"
        alt=""
        class="absolute h-[200px] bottom-[0%] z-10 sm:h-[300px] 2xl:h-[350px] rocket-rocket rocket-hide rocket"
      />
    </div> -->

    <div
      class="absolute bottom-0 left-0 z-30 flex items-center justify-center min-w-full min-h-full world-wrapper animatedWorld"
    >
      <img
        src="../../assets/img/WorldX4.png"
        alt=""
        class="absolute h-[200px] bottom-[0%] z-10 sm:h-[300px] 2xl:h-[400px] world-world world-hide"
      />
    </div>
  </section>
  <section
    class="animation sky-inside-world bg-gradient-to-b from-[#09090d] from-0% to-[#03a9f4] to-80%"
  >
    <img
      src="../../assets/img/Plane.png"
      alt=""
      class="plane top-[50%] left-0 absolute h-[100px] lg:h-[150px] 2xl:h-[200px]"
    />
  </section>
</template>

<script>
export default {
  data() {
    return {
      controller: null,
    };
  },
  mounted() {
    const flightPath = {
      curviness: 1.25,
      autoRotate: false,
      values: [
        {
          x: 0,
          y: -50,
        },
        {
          x: 0,
          y: -100,
        },
        {
          x: 0,
          y: -150,
        },
        {
          x: 0,
          y: -200,
        },
        {
          x: 0,
          y: -250,
        },
        {
          x: 0,
          y: -window.innerHeight,
        },
      ],
    };

    const tween = new TimelineLite();

    tween.add(
      TweenLite.to({}, 1, {
        ease: Power1.easeInOut,
        onUpdate: () => {
          document.body.classList.add("blue-background");
        },
        onReverseComplete: () => {
          document.body.classList.remove("blue-background");
        },
      })
    );

    tween.add(
      TweenLite.to(".space", 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    );

    // Finally, add a fade-in effect for the sky inside the world
    // Create a ScrollMagic controller
    this.controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const spaceScene = new ScrollMagic.Scene({
      triggerElement: ".spacecontainer",
      duration: 100, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tween)
      /*  .setPin(".spacecontainer") */
      .addTo(this.controller);

    const tweenSpace = new TimelineLite();

    tweenSpace.add(
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

    tweenSpace.add(
      TweenLite.to(".world-wrapper", 1, {
        scale: 5,
        ease: Linear.easeNone,
      })
    );

    this.controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const newspaceScene = new ScrollMagic.Scene({
      triggerElement: ".spacecontainer",
      duration: 1500, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenSpace)
      .setPin(".spacecontainer")
      .addTo(this.controller);

    /*  tween.add(
      TweenLite.to(".rocket-wrapper", 1, {
        bezier: flightPath,
        ease: Linear.easeInOut,
      })
    ); */

    /*     tween.add(
      TweenLite.to(".world-wrapper", 1, {
        scale: 5,
        ease: Linear.easeNone,
      })
    ); */

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
        onUpdate: () => {
          document.body.classList.remove("blue-background");
        },
        onReverseComplete: () => {
          document.body.classList.add("blue-background");
        },
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
  /*  animation: pump 4.5s infinite alternate; */
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
