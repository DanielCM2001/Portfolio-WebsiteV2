<template>
  <section
    class="flex flex-col items-center justify-center min-h-screen w-full pt-[80px] border bg-black px-[4vw]"
  >
    <div class="flex flex-col justify-center w-full break-words border">
      <h1 class="text-[2rem] text-[#F5EEE6] hideBannerSubtitle">
        Hi there! I'm Daniel
      </h1>

      <div class="overflow-hidden">
        <h1 class="text-[3.3rem] secondaryFont text-[#F5EEE6] hideBannerTitle">
          I AM A FRONT END DEVELOPER
        </h1>
      </div>

      <h1 class="text-[2.3rem] text-[#f5eee6] hideBannerSubtitle">
        +2
        <span class="text-[2rem]">Years of Experience</span>
      </h1>
      <h1 class="text-[2.3rem] text-[#f5eee6] hideBannerSubtitle">
        +7
        <span class="text-[2rem]">Projects Completed</span>
      </h1>
    </div>

    <div class="w-full break-words border">
      <div class="flex justify-end w-full">
        <div class="flex flex-col items-center justify-center">
          <img
            src="../../assets/img/ArrowRight.png"
            alt=""
            class="max-w-[80%] ml-[40%]"
          />
          <h1 class="text-[1.7rem] line-through">Mouse over</h1>
        </div>

        <!-- Add below grayscale -->

        <img
          src="../../assets/img/IdeasIcon.png"
          alt=""
          class="max-w-[150px] py-5 rotate-180"
        />
      </div>
      <div class="w-full py-10 space-y-5 MichaelAngeloBackground">
        <h1 class="text-[2.3rem]">
          Passionate about creating interactive applications and experiences on
          the web.
        </h1>

        <div class="flex flex-row items-center space-x-5">
          <h1 class="text-[1.7rem] line-through">LET'S GET IN CONTACT</h1>
          <img
            src="../../assets/img/GithubIcon.png"
            alt=""
            class="h-[40px] w-[35px]"
          />
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
  /* filter: grayscale(100%);
  opacity: 100%; */
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
