<template>
  <div>
    <section
      class="relative flex items-center justify-center min-h-screen overflow-hidden space"
      id="space"
    >
      <div class="rocket-wrapper absolute top-[60%]">
        <img src="../assets/img/Rocket.png" class="rocket h-[300px]" alt="" />
      </div>
      <div
        class="absolute bottom-0 left-0 z-10 flex items-center justify-center min-w-full min-h-full world-wrapper"
      >
        <img
          src="../assets/img/WorldX4.png"
          alt=""
          class="absolute h-[200px] bottom-[0%] z-10 world"
        />
      </div>
      <h1
        class="text-center text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[40px] lg:text-[70px] 2xl:text-[80px]"
      >
        I enjoy creating things that live
        <br class="hidden lg:flex" />
        on the internet...
      </h1>
    </section>
    <section
      class="animation sky-inside-world bg-gradient-to-b from-[#000514] from-0% to-[#03a9f4] to-80%"
    >
      <img src="../assets/img/plane.png" alt="" class="plane" />
    </section>
  </div>
</template>

<script>
export default {
  mounted() {
    /*====================== Space Section ======================*/
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
        /*         onComplete: goToNextSection, */
      })
    );

    tween.add(
      TweenLite.to(".world", 1, {
        opacity: 0,
        ease: Power1.easeInOut,
      })
    );

    // Finally, add a fade-in effect for the sky inside the world

    // Create a ScrollMagic controller
    const controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const scene = new ScrollMagic.Scene({
      triggerElement: ".space",
      duration: 1000, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tween)
      .setPin(".space")
      .addTo(controller);

    /* function goToNextSection() {
      // Transition to the next section (e.g., when the plane zoom-in animation is complete)
      const nextSection = document.querySelector(".sky-inside-world");
      window.scrollTo({
        top: nextSection.offsetTop,
        behavior: "smooth",
      });
    } */
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

.space {
  background-image: url("../assets/img/SpaceBackground.png");
  background-size: cover;
  background-repeat: no-repeat;
}

.plane {
  position: absolute;
  height: 100px;
  top: 50%;
  left: 0;
}

/* Pump Animation */
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

<!-- .world { position: absolute; height: 400px; bottom: 0%; left: 25%;
z-index: 1; } -->

<!-- .sky-inside-world {
  height: 100vh;
  width: 100%;
  background: linear-gradient(180deg, #000514 0%, #03a9f4 80%);
} -->
<!-- .world-wrapper {
   position: absolute; 
    height: 100vh;
  width: 100%; 
  bottom: 0;
  left: 0;
  z-index: 1;
} -->
