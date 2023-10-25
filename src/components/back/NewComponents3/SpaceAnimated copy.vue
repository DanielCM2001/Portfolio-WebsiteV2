<template>
  <div>
    <section
      class="relative flex flex-col items-center justify-center min-h-screen overflow-hidden spacecontainer"
    >
      <div class="bottom-0 opacity-0 space"></div>

      <!--       <img
        src="../../assets/img/Ovni.gif"
        alt=""
        class="absolute top-0 left-0 z-30 ovni-hide ovni-ovni h-[150px] sm:h-[250px] 2xl:h-[300px]"
      />

      <img
        src="../../assets/img/MoonWithoutStars.png"
        alt=""
        class="absolute h-[300px] top-0 right-0 z-30 sm:h-[400px] 2xl:h-[600px] moon-hide moon-moon"
      /> -->

      <div
        class="absolute bottom-0 left-0 z-30 flex items-center justify-center min-w-full min-h-full rocket-wrapper"
      >
        <img
          src="../../assets/img/Rocket.png"
          alt=""
          class="absolute h-[200px] bottom-[0%] z-10 sm:h-[300px] 2xl:h-[350px] rocket-rocket rocket-hide rocket"
        />
      </div>

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
        class="animatedText text-center text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[40px] lg:text-[70px] 2xl:text-[80px] z-10"
      >
        I enjoy creating things that live
        <br class="hidden lg:flex" />
        on the internet...
      </h1>
      <!--  <h1
        class="animatedText text-center text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px] lg:text-[30px] 2xl:text-[40px] z-10"
      >
        &lt;Wrapper&gt;
      </h1> -->

      <h1
        class="secondanimatedText text-center text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px] lg:text-[40px] 2xl:text-[50px] opacity-0"
      >
        &lt;/Wrapper&gt;
      </h1>
    </section>
    <section
      class="animation sky-inside-world bg-gradient-to-b from-[#000005] from-0% to-[#03a9f4] to-80%"
    >
      <img
        src="../../assets/img/Plane.png"
        alt=""
        class="plane top-[50%] left-0 absolute h-[100px] lg:h-[150px] 2xl:h-[200px]"
      />
    </section>
  </div>
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

    // First, the flight path animation for the rocket
    tween.add(
      TweenLite.to(".animatedText", 1, {
        opacity: 0,
        ease: Linear.easeNone,
        onUpdate: function () {
          if (document.querySelector(".animatedText").style.opacity == "0") {
            document.querySelector(".animatedText").classList.add("hidden");
          } else {
            document.querySelector(".animatedText").classList.remove("hidden");
          }
        },
      })
    );

    tween.add(
      TweenLite.to(".spacecontainer", 1, {
        background: "#000005",
        ease: Power1.easeInOut,
      })
    );

    tween.add(
      TweenLite.to(".space", 0, {
        opacity: 0,
        ease: Linear.easeNone,
      })
    );

    // Opacity gradually decreases to 0 as you scroll down
    tween.add(
      TweenLite.to(".space", 1, {
        opacity: 1,
        ease: Linear.easeNone,
        onUpdate: function () {
          if (document.querySelector(".space").style.opacity <= "0.4") {
            document
              .querySelector(".world-world")
              .classList.remove("world-show");
            document
              .querySelector(".rocket-rocket")
              .classList.remove("rocket-show");
            document.querySelector(".ovni-ovni").classList.remove("ovni-show");
            document.querySelector(".moon-moon").classList.remove("moon-show");
          } else {
            document.querySelector(".world-world").classList.add("world-show");
            document
              .querySelector(".rocket-rocket")
              .classList.add("rocket-show");
            document.querySelector(".ovni-ovni").classList.add("ovni-show");
            document.querySelector(".moon-moon").classList.add("moon-show");
          }
        },
      })
    );
    tween.add(
      TweenLite.to(".secondanimatedText", 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    );

    tween.add(
      TweenLite.to(".world-wrapper", 1, {
        opacity: 1,
        ease: Linear.easeNone,
      })
    );

    tween.add(
      TweenLite.to(".rocket-wrapper", 1, {
        bezier: flightPath,
        ease: Linear.easeInOut,
      })
    );

    tween.add(
      TweenLite.to(".world-wrapper", 1, {
        scale: 5,
        ease: Linear.easeNone,
      })
    );

    // Finally, add a fade-in effect for the sky inside the world
    // Create a ScrollMagic controller
    this.controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const spaceScene = new ScrollMagic.Scene({
      triggerElement: ".spacecontainer",
      duration: 3000, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tween)
      .setPin(".spacecontainer")
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

.spacecontainer {
  /* background: linear-gradient(180deg, #151517 45%, #000005 100%); */
  background: #141414;
  transition: background 0.5s; /* Add a smooth transition for the background change */
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
