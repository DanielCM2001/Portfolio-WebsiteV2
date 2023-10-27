<template>
  <section
    class="relative flex items-center justify-center min-h-screen text-white SkyAnimated"
  >
    <div class="z-0 Sky-Background"></div>
    <div class="z-10 flex flex-col mx-4 2xl:mt-40">
      <p class="text-[20px] lg:text-[25px] 2xl:text-[35px] opacity-85">
        My interest in Web Development started back in 2017
      </p>
      <p class="text-[30px] lg:text-[45px] 2xl:text-[65px]">
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
      <!--  <img
        id="windImage"
        class="hidden absolute h-[150px] bottom-[10%] right-0 z-0 sm:h-[250px] 2xl:h-[300px]"
        src="../../assets/img/Wind.png"
        alt="Wind Image"
      /> -->
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    const tweenSkyBackground = new TimelineLite();

    tweenSkyBackground.add(
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

    const controllerSky = new ScrollMagic.Controller();

    const SkyScene = new ScrollMagic.Scene({
      triggerElement: ".SkyAnimated",
      duration: 100, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenSkyBackground)
      .addTo(controllerSky);

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
        ease: Linear.easeInOut,
      })
    );

    const controllerBalloon = new ScrollMagic.Controller();

    const sceneBalloon = new ScrollMagic.Scene({
      triggerElement: ".SkyAnimated",
      duration: 1000,
      triggerHook: 0.4,
    })
      .setTween(tweenBalloon)
      .addTo(controllerBalloon);
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
  /*   background-image: url("../../assets/img/Sky.png");
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  height: 100vh;
  width: 100%; */
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
