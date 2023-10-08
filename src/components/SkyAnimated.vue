<!-- <template>
  <section
    class="flex items-center justify-center min-h-screen Sky-Background SkyAnimated"
  >
    <div class="flex flex-col mx-4 2xl:mt-40">
      <p
        class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px] lg:text-[25px] 2xl:text-[35px]"
      >
        My interest in Web Development started back in 2017
      </p>
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px] text-white">
        When I decided to try making a <br class="hidden lg:flex" />
        website for a school project
      </p>
      <p
        class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px] lg:text-[25px] 2xl:text-[35px]"
      >
        Turns out making a school project taught me a lot about web
      </p>
      <img
        src="../assets/img/Balloon.png"
        alt=""
        class="absolute h-[150px] bottom-[10%] right-20 z-0 sm:h-[250px] 2xl:h-[300px] balloon"
      />
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    const BalloonPath = {
      curviness: 1.25,
      autoRotate: false,
      values: [
        {
          x: 0,
          y: -100,
        },
        {
          x: 0,
          y: -200,
        },
        {
          x: -100,
          y: -300,
        },
        {
          x: -200,
          y: -400,
        },
      ],
    };

    const tweenBalloon = new TimelineLite();

    tweenBalloon.add(
      TweenLite.to(".balloon", 1, {
        bezier: BalloonPath,
        ease: Power1.easeInOut,
        onComplete: goToNextSection,
      })
    );

    const controllerBalloon = new ScrollMagic.Controller();

    const sceneBalloon = new ScrollMagic.Scene({
      triggerElement: ".SkyAnimated",
      duration: 1000,
      triggerHook: 0,
    })
      .setTween(tweenBalloon)
      .setPin(".SkyAnimated")
      .addTo(controllerBalloon);

    function goToNextSection() {
      // Transition to the next section (e.g., when the plane zoom-in animation is complete)
      const nextSection = document.querySelector(".designerCoder");
      window.scrollTo({
        top: nextSection.offsetTop,
        behavior: "smooth",
      });
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

.Sky-Background {
  background-image: url("../assets/img/Sky.png");
  background-size: cover;
  /*  background-position: center; */
  background-repeat: no-repeat;
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
 -->
<!-- 
<template>
  <section
    class="flex items-center justify-center min-h-screen Sky-Background SkyAnimated"
  >
    <div class="flex flex-col mx-4 2xl:mt-40">
      <p
        class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px] lg:text-[25px] 2xl:text-[35px]"
      >
        My interest in Web Development started back in 2017
      </p>
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px] text-white">
        When I decided to try making a <br class="hidden lg:flex" />
        website for a school project
      </p>
      <p
        class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px] lg:text-[25px] 2xl:text-[35px]"
      >
        Turns out making a school project taught me a lot about web
      </p>
      <img
        src="../assets/img/Balloon.png"
        alt=""
        class="absolute h-[150px] bottom-[10%] right-20 z-0 sm:h-[250px] 2xl:h-[300px] balloon"
      />
      <img
        id="windImage"
        class="hidden absolute h-[150px] bottom-[10%] right-0 z-0 sm:h-[250px] 2xl:h-[300px]"
        src="../assets/img/Wind.png"
        alt="Wind Image"
      />
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    const BalloonPath = {
      curviness: 1.25,
      autoRotate: false,
      values: [
        {
          x: 0,
          y: -100,
        },
        {
          x: 0,
          y: -200,
        },
        {
          x: -100,
          y: -300,
        },
        {
          x: -200,
          y: -400,
        },
      ],
    };

    const tweenBalloon = new TimelineLite();

    tweenBalloon.add(
      TweenLite.to(".balloon", 1, {
        bezier: BalloonPath,
        ease: Power1.easeInOut,
        /* onUpdate: checkBalloonPosition, */ // Call the checkBalloonPosition function on every update
        /* onComplete: goToNextSection, */
      })
    );

    tweenBalloon.add(
      TweenLite.to(".Sky-Background ", 1, {
        opacity: 0,
        ease: Linear.easeNone,
        /* onUpdate: checkBalloonPosition, */ // Call the checkBalloonPosition function on every update
        onComplete: goToNextSection,
      })
    );

    function checkBalloonPosition() {
      // Get the current position of the balloon (you may need to adjust the values)
      const currentPosition = tweenBalloon.time() * 1000; // Convert time to milliseconds

      // Define the point at which you want to show the wind image
      const windImageTriggerPosition = 400; // Adjust this value as needed

      if (currentPosition >= windImageTriggerPosition) {
        // Show the wind image by removing the "hidden" class
        document.getElementById("windImage").classList.remove("hidden");
      } else {
        document.getElementById("windImage").classList.add("hidden");
      }
    }

    const controllerBalloon = new ScrollMagic.Controller();

    const sceneBalloon = new ScrollMagic.Scene({
      triggerElement: ".SkyAnimated",
      duration: 1000,
      triggerHook: 0,
    })
      .setTween(tweenBalloon)
      .setPin(".SkyAnimated")
      .addTo(controllerBalloon);

    function goToNextSection() {
      // Transition to the next section (e.g., when the plane zoom-in animation is complete)
      const nextSection = document.querySelector(".designerCoder");
      window.scrollTo({
        top: nextSection.offsetTop,
        behavior: "smooth",
      });
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

.Sky-Background {
  background-image: url("../assets/img/Sky.png");
  background-size: cover;
  /*  background-position: center; */
  background-repeat: no-repeat;
}

@keyframes pump {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-20px);
  }
}
</style> -->

<template>
  <section class="flex items-center justify-center min-h-screen SkyAnimated">
    <div class="z-0 Sky-Background"></div>
    <div class="z-10 flex flex-col mx-4 2xl:mt-40">
      <p
        class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px] lg:text-[25px] 2xl:text-[35px]"
      >
        My interest in Web Development started back in 2017
      </p>
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px] text-white">
        When I decided to try making a <br class="hidden lg:flex" />
        website for a school project
      </p>
      <p
        class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px] lg:text-[25px] 2xl:text-[35px]"
      >
        Turns out making a school project taught me a lot about web
      </p>
      <img
        src="../assets/img/Balloon.png"
        alt=""
        class="absolute h-[150px] bottom-[10%] right-20 z-0 sm:h-[250px] 2xl:h-[300px] balloon"
      />
      <img
        id="windImage"
        class="hidden absolute h-[150px] bottom-[10%] right-0 z-0 sm:h-[250px] 2xl:h-[300px]"
        src="../assets/img/Wind.png"
        alt="Wind Image"
      />
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    const BalloonPath = {
      curviness: 1.25,
      autoRotate: false,
      values: [
        {
          x: 0,
          y: -100,
        },
        {
          x: 0,
          y: -200,
        },
        {
          x: -100,
          y: -300,
        },
        {
          x: -200,
          y: -400,
        },
      ],
    };

    const tweenBalloon = new TimelineLite();

    tweenBalloon.add(
      TweenLite.to(".balloon", 1, {
        bezier: BalloonPath,
        ease: Power1.easeInOut,
        /* onUpdate: checkBalloonPosition, */ // Call the checkBalloonPosition function on every update
        /* onComplete: goToNextSection, */
      })
    );

    tweenBalloon.add(
      TweenLite.to(".Sky-Background ", 1, {
        opacity: 0,
        /* ease: Linear.easeNone, */
        /* onUpdate: checkBalloonPosition, */ // Call the checkBalloonPosition function on every update
        onComplete: goToNextSection,
      })
    );

    function checkBalloonPosition() {
      // Get the current position of the balloon (you may need to adjust the values)
      const currentPosition = tweenBalloon.time() * 1000; // Convert time to milliseconds

      // Define the point at which you want to show the wind image
      const windImageTriggerPosition = 400; // Adjust this value as needed

      if (currentPosition >= windImageTriggerPosition) {
        // Show the wind image by removing the "hidden" class
        document.getElementById("windImage").classList.remove("hidden");
      } else {
        document.getElementById("windImage").classList.add("hidden");
      }
    }

    const controllerBalloon = new ScrollMagic.Controller();

    const sceneBalloon = new ScrollMagic.Scene({
      triggerElement: ".SkyAnimated",
      duration: 1000,
      triggerHook: 0,
    })
      .setTween(tweenBalloon)
      .setPin(".SkyAnimated")
      .addTo(controllerBalloon);

    function goToNextSection() {
      // Transition to the next section (e.g., when the plane zoom-in animation is complete)
      const nextSection = document.querySelector(".designerCoder");
      window.scrollTo({
        top: nextSection.offsetTop,
        behavior: "smooth",
      });
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

/* .Sky-Background {
  background-image: url("../assets/img/Sky.png");
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  height: 100vh;
} */

.Sky-Background {
  background-image: url("../assets/img/Sky.png");
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  height: 100vh;
  width: 100%;
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
