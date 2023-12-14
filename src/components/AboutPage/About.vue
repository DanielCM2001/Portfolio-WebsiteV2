<template>
  <div class="relative flex items-center justify-center">
    <!-- md:mt-[20vh] -->
    <img
      src="../../assets/img/DanielPhoto.png"
      alt=""
      class="absolute h-[350px] xs:h-[450px] rotate-90 transform -translate-y-1/4 top-[0%] z-0 md:translate-y-0 md:rotate-0 md:top-auto md:left-0 md:opacity-10 md:h-[600px] 2xl:h-[700px] 3xl:h-[800px] xl:opacity-100"
    />
    <div
      class="w-full xs:w-9/12 lg:w-full mx-5 lg:mx-[20vw] xl:mx-[25vw] static-container pt-[30vh] md:pt-[20vh] space-y-5"
    >
      <h1 class="text-[40px] md:text-[80px] text-[#f5eee6] secondaryFont">
        .about(Daniel)
      </h1>

      <p class="text-[32px]">
        A front-end Web Developer passionate about creating interactive <br />
        applications and experiences on the web.
      </p>

      <div class="flex flex-row space-x-5">
        <!--  <button class="px-8 py-3 primaryButtons">Download</button>
        <button class="px-5 py-3 primaryButtons">xd</button>
        <button class="px-5 py-3 primaryButtons">xd</button> -->
        <img
          src="../../assets/img/logo.png"
          alt=""
          class="h-[50px] w-[50px] -mt-1"
        />
        <img
          src="../../assets/img/linkedin.png"
          alt=""
          class="h-[50px] w-[50px] -mt-1"
        />
      </div>

      <div class="flex flex-col space-y-5">
        <p class="text-3xl text-white secondaryFont">Main Skills</p>

        <ul
          class="grid gap-y-[1rem] md:grid-flow-col md:grid-cols-4 md:gap-x-[2rem] opacity-50 text-2xl"
        >
          <li>Frontend, UX/UI</li>
          <li>JavaScript, CSS, HTML, Vue, React, Tailwind</li>
          <li>SQL, Solidity, Ethers.js, Cloud Computing, C#</li>
          <li>Figma, Adobe XD</li>
        </ul>
      </div>

      <div class="flex flex-col space-y-5">
        <p class="text-3xl text-white secondaryFont">Experience</p>

        <ul
          class="grid gap-y-[1rem] md:grid-flow-col md:grid-cols-4 md:gap-x-[2rem]"
        >
          <li>
            <p class="text-2xl">Web Developer</p>
            <p class="text-xl opacity-50">@Risidio</p>
            <p class="text-lg opacity-50">2023-2023</p>
          </li>
          <li>
            <p class="text-2xl">Cloud Consultant</p>
            <p class="text-xl opacity-50">@Accenture</p>
            <p class="text-lg opacity-50">2021-2021</p>
          </li>
          <li>
            <p class="text-2xl">Web Developer</p>
            <p class="text-xl opacity-50">@Sermocol</p>
            <p class="text-lg opacity-50">2021-2021</p>
          </li>
          <li>
            <p class="text-2xl">.NET Developer</p>
            <p class="text-xl opacity-50">@Sermocol</p>
            <p class="text-lg opacity-50">2021-2021</p>
          </li>
        </ul>
      </div>

      <div class="flex flex-col space-y-5">
        <p class="text-3xl text-white secondaryFont">After work</p>

        <ul
          class="grid gap-y-[1rem] md:grid-flow-col md:grid-cols-4 md:gap-x-[2rem] text-2xl"
        >
          <li>Learning guitar</li>
          <li>Working out</li>
          <li>Photography</li>
          <li>Watching Movies</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<!-- <script>
export default {
  data() {
    return {};
  },

};
</script> -->
<script>
export default {
  mounted() {
    /* const observer = new IntersectionObserver((entries) => {
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
    hiddenElementsX.forEach((el) => observer.observe(el)); */

    /* THIS ONE'S WORKING */
    /*      const observer = new IntersectionObserver((entries) => {
  entries.forEach((entry) => {
    if (entry.isIntersecting) {
      entry.target.classList.add("showBannerTitle");

      if (entry.target.clientHeight > 0) {
        // Flag to track whether showBannerTitle animation has completed
        let titleAnimationComplete = false;

        // Flag to track whether showNavBar animation has completed
        let navBarAnimationComplete = false;


        // Function to handle completion of showBannerTitle animation
        const onTitleAnimationEnd = () => {
          titleAnimationComplete = true;

          // Check if both animations have completed
          if (titleAnimationComplete && navBarAnimationComplete) {
            entry.target.classList.add("showBannerSubtitle");
          }
        };

        // Function to handle completion of showNavBar animation
        const onNavBarAnimationEnd = () => {
          navBarAnimationComplete = true;

          // Check if both animations have completed
          if (titleAnimationComplete && navBarAnimationComplete) {
            entry.target.classList.add("showBannerSubtitle");
          }
        };

        // Add event listener for the 'transitionend' event of showBannerTitle
        entry.target.addEventListener("transitionend", onTitleAnimationEnd, { once: true });

        // Add event listener for the 'transitionend' event of showNavBar
        entry.target.addEventListener("transitionend", onNavBarAnimationEnd, { once: true });
      }
    }
  });
});

    const hiddenElements = document.querySelectorAll(".hideBannerTitle");
    hiddenElements.forEach((el) => observer.observe(el));

    const hiddenElementsX = document.querySelectorAll(".hideNavBar");
    hiddenElementsX.forEach((el) => observer.observe(el));

    const hiddenElementsY = document.querySelectorAll(".hideBannerSubtitle");
    hiddenElementsY.forEach((el) => observer.observe(el));  */

    /*  const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          // Function to handle completion of showNavBar animation
          const onNavBarAnimationEnd = () => {
            entry.target.classList.add("showNavBar");
          };

          // Add event listener for the 'transitionend' event of showNavBar
          entry.target.addEventListener("transitionend", onNavBarAnimationEnd, {
            once: true,
          });
        }
      });
    });

    const hiddenElementsX = document.querySelectorAll(".hideNavBar");
    hiddenElementsX.forEach((el) => observer.observe(el)); */

    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("showNavBar");
        }
      });
    });

    const hiddenElementsX = document.querySelectorAll(".hideNavBar");
    hiddenElementsX.forEach((el) => observer.observe(el));
  },
};
</script>

<style scoped>
.primaryButtons {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}

.static-container {
  min-height: 100vh;
  /*  perspective: 900px;
  perspective-origin: 50% 50vh; */
}
</style>
