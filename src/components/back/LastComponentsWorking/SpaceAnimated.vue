<template>
  <section
    class="h-[100vh] relative flex flex-col items-center justify-center overflow-hidden space-container"
  >
    <div class="bottom-0 opacity-0 space"></div>

    <div
      class="absolute bottom-0 left-0 z-30 flex items-center justify-center w-[100vw] h-[100vh] world-wrapper animatedWorld"
    >
      <img
        src="../../../assets/img/WorldX4.png"
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
  <div
    class="h-[1vh] bg-gradient-to-b from-[#070707] from-0% to-[#070707] to-80% hidden"
  ></div>
  <section
    class="relative h-[50vh] overflow-hidden atmosphere-container bg-gradient-to-b from-[#070707] from-0% to-[#03a9f4] to-80%"
  >
    <img
      src="../../../assets/img/Plane.png"
      alt=""
      class="plane top-[50%] left-0 absolute h-[100px] lg:h-[150px] 2xl:h-[200px]"
    />
  </section>
</template>

<script>
export default {
  mounted() {
    /*====================== Space Section ======================*/
    const tweenSpace = new TimelineLite();

    tweenSpace.add(
      TweenLite.to(".space", 0, {
        opacity: 0,
        ease: Linear.easeNone,
      })
    );

    tweenSpace.add(
      TweenLite.to(".space", 1, {
        opacity: 1,
        ease: Linear.easeNone,

        onUpdate: function () {
          const spaceElement = document.querySelector(".space");
          const darkspaceBackgroundElement = document.querySelector(
            ".darkspace-background"
          );
          const worldWorldElement = document.querySelector(".world-world");

          if (spaceElement && spaceElement.style.opacity !== "0") {
            // Add the class to the body
            document.body.classList.add("darkspace-background");

            // Change the background color of the class
            if (darkspaceBackgroundElement) {
              darkspaceBackgroundElement.style.backgroundColor = "#070707"; // Set the desired background color
            }

            if (worldWorldElement) {
              worldWorldElement.classList.add("world-show");
            }
          } else {
            // Remove the class from the body
            document.body.classList.remove("darkspace-background");

            // Remove the background color style
            if (darkspaceBackgroundElement) {
              darkspaceBackgroundElement.style.backgroundColor = null;
            }

            if (worldWorldElement) {
              worldWorldElement.classList.remove("world-show");
            }
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

    const controllerSpace = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const sceneSpace = new ScrollMagic.Scene({
      triggerElement: ".space-container",
      duration: 1500, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenSpace)
      .setPin(".space-container")
      .addTo(controllerSpace);
    /*====================== Plane Section ======================*/

    const planeflightPath = {
      curviness: 1.25,
      autoRotate: true,
      values: [
        {
          x: window.innerWidth,
          y: 0,
        },
      ],
    };

    const tweenPlanePath = new TimelineLite();

    tweenPlanePath.add(
      TweenLite.to(".plane", 1, {
        bezier: planeflightPath,
        ease: Power1.easeInOut,
      })
    );

    const controllerPlanePath = new ScrollMagic.Controller();

    const scenePlanePath = new ScrollMagic.Scene({
      triggerElement: ".atmosphere-container",
      duration: 1000,
      triggerHook: 0,
    })
      .setTween(tweenPlanePath)
      .addTo(controllerPlanePath);
  },
  beforeUnmount() {
    document.body.classList.remove("darkspace-background");
  },
};
</script>

<style scoped>
.space {
  background-image: url("../../../assets/img/NewSpaceBackground.png");
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
</style>
