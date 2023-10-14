<template>
  <div>
    <section
      class="relative flex items-center justify-center min-h-screen overflow-hidden spacecontainer"
    >
      <div class="bottom-0 space"></div>

      <img
        src="../../assets/img/Ovni.gif"
        alt=""
        class="absolute hide h-[150px] top-[0%] left-0 z-0 sm:h-[250px] 2xl:h-[300px]"
      />
      <img
        src="../../assets/img/moon.png"
        alt=""
        class="absolute h-[300px] top-[0%] right-0 z-0 sm:h-[400px] 2xl:h-[600px]"
      />

      <div class="rocket-wrapper absolute top-[60%] z-20">
        <img
          src="../../assets/img/Rocket.png"
          class="rocket h-[300px] 2xl:h-[400px]"
          alt=""
        />
      </div>
      <div
        class="absolute bottom-0 left-0 z-30 flex items-center justify-center min-w-full min-h-full world-wrapper"
      >
        <img
          src="../../assets/img/WorldX4.png"
          alt=""
          class="absolute h-[200px] bottom-[0%] z-10 world sm:h-[300px] 2xl:h-[400px]"
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
    <section
      class="animation sky-inside-world bg-gradient-to-b from-[#000005] from-0% to-[#03a9f4] to-80%"
    >
      <img
        src="../../assets/img/plane.png"
        alt=""
        class="plane top-[50%] left-0 absolute h-[100px] lg:h-[150px] 2xl:h-[200px]"
      />
    </section>
  </div>
</template>

<script>
export default {
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
      TweenLite.to(".rocket", 1, {
        bezier: flightPath,
        ease: Power1.easeInOut,
      })
    );

    // Then, add a scaling effect for the world at the end of the rocket animation
    tween.add(
      TweenLite.to(".world-wrapper", 1, {
        scale: 5,
        ease: Linear.easeNone,
      })
    );

    // Finally, add a fade-in effect for the sky inside the world

    // Create a ScrollMagic controller
    const controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const scene = new ScrollMagic.Scene({
      triggerElement: ".spacecontainer",
      duration: 2000, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tween)
      .setPin(".spacecontainer")
      .addTo(controller);

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
};
</script>

<style scoped>
.animation {
  position: relative;
  height: 100vh;
  overflow: hidden;
}

.spacecontainer {
  background: linear-gradient(180deg, #151517 50%, #000005 100%);
}

.space {
  background-image: url("../../assets/img/StarsBackg.png");
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  height: 100vh;
  width: 100%;
}

.rocket-wrapper {
  animation: pump 1.5s infinite alternate;
}

@keyframes pump {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-20px);
  }
}
</style>
