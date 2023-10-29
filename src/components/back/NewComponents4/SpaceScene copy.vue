<template>
  <section
    class="h-[100vh] relative flex flex-col items-center justify-center overflow-hidden spacecontainer"
  >
    <div class="bottom-0 opacity-0 space"></div>

    <div
      class="absolute bottom-0 left-0 z-30 flex items-center justify-center min-w-full min-h-full world-wrapper animatedWorld"
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
</template>

<script>
export default {
  data() {
    return {
      controller: null,
    };
  },
  mounted() {
    const tweenSpaceBackground = new TimelineLite();

    tweenSpaceBackground.add(
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

    const spaceBackgroundScene = new ScrollMagic.Scene({
      triggerElement: ".spacecontainer",
      duration: 100, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenSpaceBackground)
      .addTo(this.controller);

    /* =================== World Animated Scene ========================= */
    const tweenSpaceWorld = new TimelineLite();

    tweenSpaceWorld.add(
      TweenLite.to(".space", 0, {
        opacity: 0,
        ease: Linear.easeNone,
      })
    );

    tweenSpaceWorld.add(
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

    tweenSpaceWorld.add(
      TweenLite.to(".world-wrapper", 1, {
        scale: 5,
        ease: Linear.easeNone,
      })
    );

    this.controller = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const spaceWorldScene = new ScrollMagic.Scene({
      triggerElement: ".spacecontainer",
      duration: 1500, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tweenSpaceWorld)
      .setPin(".spacecontainer")
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
