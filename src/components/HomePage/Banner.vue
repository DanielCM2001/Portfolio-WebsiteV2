<!-- <section class="flex flex-col items-center justify-center h-[100vh] w-full">
    <div
      class="z-20 flex items-center justify-center w-full mt-20 border h-1/2"
    >
      <h1 class="uppercase text-[35px]">
        I AM A FRONT END <br />
        DEVELOPER
      </h1>
    </div>

    <div class="absolute flex items-center justify-center w-full h-full border">
      <img
        src="../../assets/img/BannerCircle.png"
        alt="Banner image"
        class="w-full max-w-xl"
      />
    </div>

    
    <div class="flex flex-col items-center justify-center w-full border h-1/2">
      <div class="mt-20">
        <h1 class="text-2xl">Hi there! I'm Daniel</h1>
        <h1 class="text-2xl">
          Passionate about creating interactive applications and experiences on
          the web.
        </h1>
      </div>
    </div>
  </section> -->

<!-- <div
      class="z-20 flex items-center justify-center w-full mt-20 border h-1/2"
    >
      <h1 class="uppercase text-[35px]">
        I AM A FRONT END <br />
        DEVELOPER
      </h1>
    </div>

    <div class="absolute flex items-center justify-center w-full h-full border">
      <img
        src="../../assets/img/BannerCircle.png"
        alt="Banner image"
        class="w-full max-w-xl"
      />
    </div> -->
<template>
  <section
    class="flex flex-col items-center justify-center h-[100vh] w-full border banner-section"
  >
    <div
      class="flex items-center justify-center w-full h-[100vh] text-center border"
    >
      <div class="flex flex-col items-center justify-center pt-20">
        <h1
          class="uppercase text-[36px] lg:text-[110px] z-10 animatedText mt-10"
        >
          I AM A FRONT END <br />
          DEVELOPER
        </h1>
        <img
          src="../../assets/img/BannerCircle.png"
          alt="Banner image"
          class="z-0 w-full max-w-sm -mt-52 lg:max-w-2xl animatedText"
        />
      </div>

      <!-- flex flex-col items-center justify-center -->
    </div>
    <div
      class="lg:absolute lg:top-[65%] left-0 flex items-center justify-center lg:w-1/3 bg-gray-500 border w-full"
    >
      <div
        class="flex flex-col ml-[2vw] 2xl:ml-[6vw] w-full bg-gray-950 space-y-5"
      >
        <h1 class="text-3xl">
          Hi there! I'm <span class="text-[#C3023A]">Daniel</span>
        </h1>
        <h1 class="text-2xl">
          Passionate about creating interactive applications and
          <span class="text-[#C3023A]">experiences on the web.</span>
        </h1>

        <div
          class="flex flex-col py-5 space-y-5 sm:flex-row sm:space-y-0 sm:space-x-5 max-w-7xl"
        >
          <div class="flex flex-row w-full space-x-5">
            <p class="text-5xl md:text-4xl lg:text-5xl text-[#C3023A]">+8</p>
            <p class="text-lg md:text-md lg:text-lg">Projects completed</p>
          </div>

          <div class="flex flex-row w-full space-x-5">
            <p class="text-5xl md:text-4xl lg:text-5xl text-[#C3023A]">2</p>
            <p class="text-lg md:text-md lg:text-lg">Years of Experience</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    /*     let tween_Text = gsap.timeline({
      scrollTrigger: {
        trigger: ".banner-section",
        scrub: 2, // smooth scrubbing, takes 1 second to "catch up" to the scrollbar
        start: "top top",
        end: "bottom top",
      },
    });

    tween_Text.to(".animatedText", {
      transform: "translate(0%, 0%) translate3d(0px, 0px, 0px) scale(1)",
    });
    tween_Text.to(
      ".animatedText",
      {
        transform: "translate(0%, -150%) translate3d(0px, 0px, 0px) scale(1)",
      },
      "0"
    );

    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("showAnimation");
        }
      });
    });

    const hiddenElements = document.querySelectorAll(".hideAnimation");
    hiddenElements.forEach((el) => observer.observe(el)); */

    /* const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("showAnimation");

          // Disconnect the observer after animation is triggered
          observer.disconnect();
        }
      });
    });

    const hiddenElements = document.querySelectorAll(".hideAnimation");
    hiddenElements.forEach((el) => observer.observe(el)); */

    gsap.to(".animatedText", {
      scale: 1,
    });

    // GSAP Animation
    let tween_Text = gsap.timeline({
      scrollTrigger: {
        trigger: ".banner-section",
        scrub: 2,
        start: "top top",
        end: "bottom top",
      },
    });

    tween_Text.to(".animatedText", {
      transform: "translate(0%, 0%) translate3d(0px, 0px, 0px) scale(1)",
    });

    tween_Text.to(
      ".animatedText",
      {
        transform: "translate(0%, -150%) translate3d(0px, 0px, 0px) scale(1)",
      },
      "0"
    );
  },
};
</script>

<style scoped>
.hideAnimation {
  transform: translateY(-150%);
  transition: all 1s;
}

.showAnimation {
  transform: translateY(0);
}

.primaryButtons {
  border-radius: 20px;
  background: #c3023a;
  box-shadow:
    0px 5px 5px 0px #c3023a inset,
    0px 4px 50px 0px #c3023a;
}
</style>
