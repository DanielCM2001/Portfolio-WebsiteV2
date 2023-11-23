<!-- <template>
  <section
    class="flex flex-col items-center justify-center min-h-screen w-full pt-[80px] border bg-black px-[4vw]"
  >
    <div class="flex flex-col justify-center w-full break-words border">
      <h1 class="text-[8.5vw] xs:text-[2.6rem] text-[#F5EEE6]">
        Hi there! I'm Daniel
      </h1>

      <div class="overflow-hidden">
        <h1 class="text-[14vw] xs:text-[4.3rem] secondaryFont text-[#F5EEE6]">
          I AM A FRONT END DEVELOPER
        </h1>
      </div>

      <h1 class="text-[9.8vw] xs:text-[3rem] text-[#f5eee6]">
        +2
        <span class="text-[8.5vw] xs:text-[2.6rem]">Years of Experience</span>
      </h1>
      <h1 class="text-[9.8vw] xs:text-[3rem] text-[#f5eee6]">
        +7
        <span class="text-[8.5vw] xs:text-[2.6rem]">Projects Completed</span>
      </h1>
    </div>

    <div class="flex flex-col w-full break-words border">
      <div class="flex justify-end w-full">
        <div class="flex flex-col items-center justify-center">
          <img
            src="../../assets/img/ArrowRight.png"
            alt=""
            class="max-w-[80%] ml-[40%]"
          />
          <h1 class="text-[7.5vw] xs:text-[2.3rem] line-through">Mouse over</h1>
        </div>

        <img
          src="../../assets/img/IdeasIcon.png"
          alt=""
          class="max-w-[40%] xs:max-w-[200px] py-5 rotate-180"
        />
      </div>

      <div class="w-full py-10 space-y-5 MichaelAngeloBackground">
        <h1 class="text-[9.8vw] xs:text-[3rem]">
          Passionate about creating interactive applications and experiences on
          the web.
        </h1>

        <div class="flex flex-row items-center space-x-5">
          <h1 class="text-[7.5vw] xs:text-[2.3rem] line-through">
            LET'S GET IN CONTACT
          </h1>
          <img
            src="../../assets/img/GithubIcon.png"
            alt=""
            class="h-[40px] w-[35px]"
          />
        </div>
      </div>
    </div>
  </section>
</template> -->

<template>
  <section
    class="flex flex-row items-center justify-center min-h-screen w-full pt-[80px] px-[4vw]"
  >
    <!--   <img
      class="absolute z-0 w-full h-full MichaelAngeloBackground grayscale opacity-10"
    /> -->
    <div class="z-10 flex items-stretch w-full">
      <div class="flex flex-col justify-center break-words w-[70%]">
        <h1 class="text-[36px] secondaryFont text-[#f5eee6]">
          Hi there! I'm Daniel
        </h1>

        <div class="overflow-hidden">
          <h1 class="text-[140px] uppercase secondaryFont text-[#F5EEE6]">
            Designer <span class="text-[64px]">&</span> <br />
            Developer
            <!--   I AM A FRONT <br />
            END <br />
            DEVELOPER -->
          </h1>
        </div>

        <h1 class="text-[40px] text-[#f5eee6]">
          +2
          <span class="text-[36px]">Years of Experience</span>
        </h1>
        <h1 class="text-[40px] text-[#f5eee6]">
          +7
          <span class="text-[36px]">Projects Completed</span>
        </h1>
      </div>

      <!-- <div class="flex justify-center items-center h-[60%]">
          <div class="flex flex-col items-center justify-center">
            <img
              src="../../assets/img/ArrowRight.png"
              alt=""
              class="max-w-[80%] ml-[40%]"
            />
            <h1 class="text-[32px] line-through">Mouse over</h1>
          </div>

          <img
            src="../../assets/img/IdeasIcon.png"
            alt=""
            class="max-w-[50%] max-h-[50%] rotate-180"
          />
        </div> -->

      <div class="break-words flex flex-col w-[30%]">
        <!-- Left side content -->
        <div class="flex justify-center items-center h-[50%] relative">
          <div
            class="absolute left-0 flex flex-col items-center justify-center"
          >
            <img
              src="../../assets/img/ArrowRight.png"
              alt=""
              class="max-w-[80%] ml-[40%]"
            />
            <h1 class="text-[32px] line-through">Click here</h1>
          </div>

          <img
            src="../../assets/img/LightBulb.png"
            alt=""
            class="max-w-[100%] max-h-[100%] z-10"
          />

          <!--  <div
            class="w-[15px] h-[100%] -mt-[100%] bg-[#b9acac] absolute z-0 border-[#000000] border-4"
          ></div> -->
          <div
            class="w-[14px] h-[150%] -top-[100%] bg-[#b9acac] absolute z-0 border-[#201a27] border-[3px]"
          ></div>
        </div>

        <!-- mx-[-40px] px-[40px] MichaelAngeloBackground--><!-- px-10  -->
        <div class="py-10 space-y-5 h-[50%] px-10 MichaelAngeloBackground">
          <h1 class="text-[40px]">
            Passionate about creating interactive applications and experiences
            on the web.
          </h1>

          <div class="flex flex-row items-center space-x-5">
            <h1 class="text-[32px] line-through">LET'S GET IN CONTACT</h1>
            <img
              src="../../assets/img/GithubIcon.png"
              alt=""
              class="h-[40px] w-[35px] -mt-1"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    // Check if the clientHeight is greater than 0
    /*  if (entry.target.clientHeight > 0) {
            // Add an event listener for the 'transitionend' event
            entry.target.addEventListener(
              "transitionend",
              () => {
                entry.target.classList.add("showBannerSubtitle");
              },
              { once: true }
            ); // { once: true } ensures the event listener is only triggered once
          } */

    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("showBannerTitle");

          if (entry.target.clientHeight > 0) {
            // Add an event listener for the 'transitionend' event
            entry.target.addEventListener(
              "transitionend",
              () => {
                entry.target.classList.add("showNavBar");

                // Add another event listener for the 'transitionend' event of showNavBar
                entry.target.addEventListener(
                  "transitionend",
                  () => {
                    // Add showBannerSubtitle after showNavBar animation ends
                    entry.target.classList.add("showBannerSubtitle");
                  },
                  { once: true }
                );
              },
              { once: true }
            ); // { once: true } ensures the event listener is only triggered once
          }
        }
      });
    });

    const hiddenElements = document.querySelectorAll(".hideBannerTitle");
    hiddenElements.forEach((el) => observer.observe(el));

    const hiddenElementsY = document.querySelectorAll(".hideBannerSubtitle");
    hiddenElementsY.forEach((el) => observer.observe(el));

    const hiddenElementsX = document.querySelectorAll(".hideNavBar");
    hiddenElementsX.forEach((el) => observer.observe(el));
  },
};
</script>

<style scoped>
.MichaelAngeloBackground {
  background-image: url("../../assets/img/MichaelAngeloBanner.png");
  background-size: cover;
}

/* .hideBannerTitle {
  opacity: 0;
  rotate: 15deg;
  transform: translateY(80%);
  transition: all 1s;
}

.showBannerTitle {
  opacity: 1;
  rotate: 0deg;
  transform: translateY(0);
}

.hideBannerSubtitle {
  opacity: 0;
  transform: translateY(10%);
  transition: all 1s;
}

.showBannerSubtitle {
  transform: translateY(0%);
  opacity: 1;
} */
</style>
