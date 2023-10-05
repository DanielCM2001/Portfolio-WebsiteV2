<template>
  <div>
    <section class="flex items-center justify-center animation space">
      <div class="rocket-wrapper absolute top-[60%]">
        <img src="../assets/img/Rocket.png" class="rocket h-[300px]" alt="" />
      </div>
      <div
        class="absolute bottom-0 left-0 z-10 flex items-center justify-center min-w-full min-h-full world-wrapper"
      >
        <img
          src="../assets/img/WorldX4.png"
          alt=""
          class="absolute h-[200px] bottom-[0%] z-10 world-world"
        />
      </div>
      <h1
        class="text-center text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)]"
      >
        I enjoy creating things that live
        <br />
        on the internet...
      </h1>
    </section>
    <section
      class="animation bg-gradient-to-b from-[#000514] from-0% to-[#03a9f4] to-80%"
    ></section>
    <section
      class="flex items-center justify-center min-h-full Sky-Background animation"
    >
      <div class="flex flex-col mx-4">
        <p class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)]">
          My interest in Web Development started back in 2017
        </p>
        <p>When I decided to try making a website for a school project</p>
        <p class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)]">
          Turns out making a school project taught me a lot about web
        </p>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  /*  mounted() {
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
        onComplete: goToNextSection,
      })
    );

    tween.add(
      TweenLite.to(".world-world", 1, {
        opacity: 0,
        ease: Power1.easeInOut,
      })
    );

    // Finally, add a fade-in effect for the sky inside the world

    // Create a ScrollMagic controller
    const controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const scene = new ScrollMagic.Scene({
      triggerElement: ".animation",
      duration: 1000, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tween)
      .setPin(".animation")
      .addTo(controller);

    function goToNextSection() {
      // Transition to the next section (e.g., when the plane zoom-in animation is complete)
      const nextSection = document.querySelector(".sky-inside-world");
      window.scrollTo({
        top: nextSection.offsetTop,
        behavior: "smooth",
      });
    }
  }, */
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
  /*  background-position: center; */
  background-repeat: no-repeat;
}

/* Pump Animation */
.rocket-wrapper {
  animation: pump 1.5s infinite alternate;
}

.world-wrapper {
  /* position: absolute; */
  /*   height: 100vh;
  width: 100%; 
  bottom: 0;
  left: 0;
  z-index: 1;*/
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

<!-- .world-world { position: absolute; height: 400px; bottom: 0%; left: 25%;
z-index: 1; } -->

<!-- .sky-inside-world {
  height: 100vh;
  width: 100%;
  background: linear-gradient(180deg, #000514 0%, #03a9f4 80%);
} -->
