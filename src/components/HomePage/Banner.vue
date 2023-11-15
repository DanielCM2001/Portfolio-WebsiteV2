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
  <!-- lg:h-[100vh] -->
  <section
    class="flex flex-col items-center justify-center min-h-screen w-full border banner-section pt-[70px]"
  >
    <!--  <div
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
    </div> -->
    <!-- <h1 class="uppercase text-[36px] lg:text-[110px] z-10 animatedText">
          I AM A FRONT END <br />
          DEVELOPER
        </h1>
        <img
          src="../../assets/img/BannerCircle.png"
          alt="Banner image"
          class="z-0 w-full max-w-sm -mt-20 xs:max-w-md lg:-mt-52 lg:max-w-2xl animatedText"
        />
        <img
          src="../../assets/img/AvatarBigger.png"
          alt="Banner image"
          class="absolute z-20 w-full max-w-sm xs:max-w-md -mt-1 lg:mt-20 lg:max-w-[650px] animatedText"
        /> --><!-- Might join the image above with the circle after, also need to fix the avatar borders below -->

    <!--lg:text-[6vw]   circle sm:-mt-[20%] sm:max-w-[60%]-->

    <!-- lg:h-[100vh] -->
    <div class="flex items-center justify-center w-full text-center border">
      <div class="flex flex-col items-center justify-center bg-black">
        <h1
          class="uppercase text-[9.5vw] 2md:text-[8vw] xl:text-[7vw] 2xl:text-[6vw] z-10"
        >
          I AM A FRONT END <br />
          DEVELOPER
        </h1>
        <img
          src="../../assets/img/BannerCircle.png"
          alt="Banner image"
          class="z-0 w-full max-w-[75%] -mt-[20%] lg:max-w-[65%]"
        />
      </div>
    </div>
    <!-- ========================================== -->

    <!-- lg:absolute lg:top-[65%] lg:w-1/3 -->
    <div
      class="lg:absolute lg:top-[65%] lg:w-1/3 lg:left-[2vw] flex items-center justify-center w-full bg-gray-500 border"
    >
      <!-- mx-[4vw] lg:mx-[4vw] 2xl:mx-0 2xl:ml-[6vw] -->
      <div class="flex flex-col mx-[4vw] w-full space-y-5 bg-gray-950">
        <h1 class="text-3xl 3xl:text-[1.5vw] 3xl:leading-[2vw]">
          Hi there! I'm <span class="text-[#C3023A]">Daniel</span>
        </h1>
        <!-- THE VW IS NOT WORKING WHEN 4K, FIX IT TOMORROW -->
        <!-- 3xl:text-[1.5vw] -->

        <!-- text-[6.5vw] xs:text-[4.5vw] -->
        <!-- 3xl:text-[1.5vw] 3xl:leading-[2vw] -->
        <h1 class="text-2xl 3xl:text-[1.25vw] 3xl:leading-[1.65vw]">
          Passionate about creating interactive applications and
          <span class="text-[#C3023A]">experiences on the web.</span>
        </h1>

        <div
          class="flex flex-col py-5 space-y-5 sm:flex-row sm:space-y-0 sm:space-x-5"
        >
          <div class="flex flex-row items-center w-full space-x-5">
            <p
              class="text-5xl 3xl:text-[2.5vw] 3xl:leading-[3vw] text-[#C3023A]"
            >
              +8
            </p>
            <p class="text-lg 3xl:text-[0.95vw] 3xl:leading-[1.3vw]">
              Projects completed
            </p>
          </div>

          <div class="flex flex-row items-center w-full space-x-5">
            <p
              class="text-5xl 3xl:text-[2.5vw] 3xl:leading-[3vw] text-[#C3023A]"
            >
              2
            </p>
            <p class="text-lg 3xl:text-[0.95vw] 3xl:leading-[1.3vw]">
              Years of Experience
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- <div
      class="lg:absolute lg:top-[65%] left-0 flex items-center justify-center lg:w-1/3 bg-gray-500 border w-full"
    >
      <div
        class="flex flex-col mx-[4vw] 2xl:mx-0 2xl:ml-[6vw] w-full bg-gray-950 space-y-5"
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
          <div class="flex flex-row items-center w-full space-x-5">
            <p class="text-5xl md:text-4xl lg:text-5xl text-[#C3023A]">+8</p>
            <p class="text-lg md:text-md lg:text-lg">Projects completed</p>
          </div>

          <div class="flex flex-row items-center w-full space-x-5">
            <p class="text-5xl md:text-4xl lg:text-5xl text-[#C3023A]">2</p>
            <p class="text-lg md:text-md lg:text-lg">Years of Experience</p>
          </div>
        </div>
      </div>
    </div> -->
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
