<template>
  <div>
    <section
      class="relative flex flex-col items-center justify-center min-h-screen overflow-hidden spacecontainer"
    >
      <div class="bottom-0 opacity-0 space"></div>

      <div
        class="absolute bottom-0 left-0 z-30 flex items-center justify-center min-w-full min-h-full world-wrapper hide animatedWorld"
      >
        <img
          src="../../assets/img/WorldX4.png"
          alt=""
          class="absolute h-[200px] bottom-[0%] z-10 world sm:h-[300px] 2xl:h-[400px]"
        />
      </div>
      <h1
        class="animatedText text-center text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[40px] lg:text-[70px] 2xl:text-[80px] z-10"
      >
        I enjoy creating things that live
        <br class="hidden lg:flex" />
        on the internet...
      </h1>
      <h1
        class="animatedText text-center text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px] lg:text-[30px] 2xl:text-[40px] z-10"
      >
        &lt;Wrapper&gt;
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
    const tween = new TimelineLite();

    // First, the flight path animation for the rocket
    tween.add(
      TweenLite.to(".animatedText", 1, {
        opacity: 0,
        ease: Linear.easeNone,
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
        onComplete: function () {
          // Add the "show" class to your element when the animation completes
          document.querySelector(".animatedWorld").classList.add("show");
        },
      })
    );

    // Finally, add a fade-in effect for the sky inside the world
    // Create a ScrollMagic controller
    const controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const spaceScene = new ScrollMagic.Scene({
      triggerElement: ".spacecontainer",
      duration: 1000, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tween)
      .setPin(".spacecontainer")
      .addTo(controller);
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
  background: #151517;
  transition: background 0.5s; /* Add a smooth transition for the background change */
}

.space {
  background-image: url("../../assets/img/StarsBackg.png");
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  height: 100vh;
  width: 100%;
  animation: pump 4.5s infinite alternate;
}

.rocket-wrapper {
  /*  animation: pump 4.5s infinite alternate; */
}

@keyframes pump {
  0% {
    /*  transform: translateY(0); */
    transform: translate3d(0);
  }
  100% {
    /*   transform: translateY(-20px); */
    transform: translate3d(12px, -22px, -25px);
  }
}
</style>
