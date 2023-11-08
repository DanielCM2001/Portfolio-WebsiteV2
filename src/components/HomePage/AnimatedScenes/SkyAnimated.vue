<template>
  <!-- <div class="h-[25vh] newskycontainer"></div> -->
  <section
    class="relative flex flex-col items-center justify-center text-[#dbdbdb] skycontainer"
  >
    <!-- First Phrase comes here -->
    <!-- bg-[#03a9f4] -->
    <div class="h-[100vh] newskycontainer"></div>
    <div
      class="h-[100vh] flex items-center justify-center w-full relative overflow-hidden"
    >
      <div class="z-30 flex flex-col mx-4">
        <p class="text-[20px] lg:text-[25px] 2xl:text-[25px] opacity-85">
          My interest in Web Development started back in 2017
        </p>
        <!--  <p class="text-[30px] lg:text-[45px] 2xl:text-[65px] font-bold">
          When I decided to
          <span class="text-[#682ae9] font-bold">
            try making a <br class="hidden lg:flex" />
            website for a school project</span
          >
        </p> -->
        <!-- a9337c -->
        <!-- cf3e98 -->
        <!-- a921ff -->
        <p class="text-[30px] lg:text-[45px] 2xl:text-[65px] font-bold">
          When I decided to
          <span class="text-[#C3023A] font-bold">
            make a <br class="hidden lg:flex" />
            website for a school project</span
          >
        </p>

        <!-- When I decided to make a website for a school project -->
        <p class="text-[20px] lg:text-[25px] 2xl:text-[25px] opacity-85">
          Turns out making a school project taught me a lot about web
        </p>
      </div>
    </div>

    <!--  Second Phrase comes here -->
    <!-- bg-gradient-to-b from-[#03a9f4] from-0% to-[#03a9f4] to-80% -->
    <div class="h-[100vh] flex items-center justify-center w-full relative">
      <div
        class="z-30 flex flex-col items-stretch justify-center w-full pl-5 pr-5 max-w-screen-2xl md:flex-row md:space-x-10"
      >
        <!-- Left Side (Designer) -->
        <div
          class="flex flex-col items-center justify-center w-full text-center"
        >
          <p class="text-[70px] lg:text-[90px] 2xl:text-[120px] font-bold hide">
            Designer
          </p>

          <p class="text-xl lg:text-2xl 2xl:text-3xl hide">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et
            dolore magna aliqua. Ut enim ad minim veniam, qu
          </p>
        </div>

        <!-- Right Side (Developer) -->
        <div
          class="flex flex-col items-center justify-center w-full text-center"
        >
          <p class="text-[70px] lg:text-[90px] 2xl:text-[120px] font-bold hide">
            Coder++
          </p>

          <p class="text-xl lg:text-2xl 2xl:text-3xl hide">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, re et
            dolore magna aliqua. Ut enim ad minim veniam, qu
          </p>
        </div>
      </div>
    </div>

    <!-- Animated Layers -->
    <img
      src="../../../assets/img/HouseBalloonsFirst.png"
      alt=""
      class="fixed top-[60%] right-[0%] h-[150px] sm:h-[250px] 2xl:h-[600px] balloon z-20 opacity-0"
    />

    <img
      src="../../../assets/img/CloudOne.png"
      alt="Fixed Image"
      class="fixed bottom-0 left-0 z-10 opacity-0 cloudOne"
      style="transform: translate(0%, 60%) translate3d(0px, 0px, 0px) scale(1)"
    />

    <img
      src="../../../assets/img/CloudTwo.png"
      alt="Fixed Image"
      class="fixed bottom-0 right-0 z-10 opacity-0 cloudTwo"
      style="transform: translate(0%, 80%) translate3d(0px, 0px, 0px) scale(1)"
    />

    <img
      src="../../../assets/img/LeftMountain.png"
      alt="Fixed Image"
      class="fixed bottom-0 z-20 blur-[2px] opacity-0 left-0 grassOne"
      style="transform: translate(0%, 30%) translate3d(0px, 0px, 0px) scale(1)"
    />

    <img
      src="../../../assets/img/RightMountain.png"
      alt="Fixed Image"
      class="fixed bottom-0 z-20 blur-[2px] opacity-0 right-0 grassTwo"
      style="transform: translate(0%, 20%) translate3d(0px, 0px, 0px) scale(1)"
    />
  </section>

  <!-- The "Gap" div below is used to make the Animated Layers below disappear by changing their opacity back to 0 -->
  <!-- bg-gradient-to-b from-[#03a9f4] from-0% to-[#66B7DC] to-80% -->
  <div class="gap h-[100vh]"></div>
</template>

<script>
export default {
  mounted() {
    /* const sections = gsap.utils.toArray(".section");
    const body = document.querySelector("body");

    sections.forEach((element, index) => {
      console.log("height", element.offsetHeight);
      let className = element.dataset.name;
      let previousClassName;
      let nextClassName;
      if (index > 0) {
        previousClassName = sections[index - 1].dataset.name;
      }
      if (index < sections.length - 1) {
        nextClassName = sections[index + 1].dataset.name;
      }
      ScrollTrigger.create({
        trigger: element,
        start: "top bottom",
        end: "bottom top",
        onEnter: () => {
          body.classList.remove(previousClassName);
          body.classList.add(className);
        },
        onEnterBack: () => {
          body.classList.remove(previousClassName);
          body.classList.remove(nextClassName);
          body.classList.add(className);
        },
        onLeaveBack: () => {
          body.classList.remove(className);
        },
        onLeave: () => {
          body.classList.remove(className);
        },
        markers: true,
      });
    }); */
    const navbar = document.querySelector(".navbar-container");

    ScrollTrigger.create({
      trigger: ".skycontainer",
      start: "top top",
      end: "bottom top",
      onEnter: () => {
        /*  body.classList.remove(previousClassName);
        body.classList.add(className); */
        document.body.classList.add("skySpace-background");
        /*  navbar.classList.remove("navbar-container"); */
        navbar.classList.add("navbar-container-sky");
      },
      onEnterBack: () => {
        /* body.classList.remove(previousClassName);
        body.classList.remove(nextClassName);
        body.classList.add(className); */
        document.body.classList.add("skySpace-background");
        /*   navbar.classList.remove("navbar-container"); */
        navbar.classList.add("navbar-container-sky");
      },
      onLeaveBack: () => {
        /*   body.classList.remove(className); */
        document.body.classList.remove("skySpace-background");
        navbar.classList.remove("navbar-container-sky");
      },
      onLeave: () => {
        /*   body.classList.remove(className); */
        document.body.classList.remove("skySpace-background");
        navbar.classList.remove("navbar-container-sky");
      },
      /* markers: true, */
    });

    /* ============================= */
    const tween_Layers_Opacity_True = new TimelineLite();

    tween_Layers_Opacity_True.add(
      TweenLite.to(
        [".cloudOne", ".cloudTwo", ".balloon", ".grassOne", ".grassTwo"],
        0,
        {
          opacity: 0,
        }
      )
    );

    tween_Layers_Opacity_True.add(
      TweenLite.to(
        [".cloudOne", ".cloudTwo", ".balloon", ".grassOne", ".grassTwo"],
        1,
        {
          opacity: 1,
          /*  onUpdate: function () {
            const spaceElement = document.querySelector(".cloudOne");
            const sky = document.querySelector(".something");
            const darkspaceBackgroundElement = document.querySelector(
              ".skySpace-background"
            );

            if (spaceElement && spaceElement.style.opacity !== "0") {
              // Add the class to the body

              sky.classList.remove("default-background");

              sky.classList.add("skySpace-background");

              // Change the background color of the class
              if (darkspaceBackgroundElement) {
                darkspaceBackgroundElement.style.backgroundColor = "#070707"; // Set the desired background color
              }
            } else {
              // Remove the class from the body
              sky.classList.remove("skySpace-background");
              sky.classList.add("default-background");

              // Remove the background color style
              if (darkspaceBackgroundElement) {
                darkspaceBackgroundElement.style.backgroundColor = null;
              }
            }
          }, */

          /*  onUpdate: function () {
            const spaceElement = document.querySelector(".cloudOne");
            const darkspaceBackgroundElement = document.querySelector(
              ".skySpace-background"
            );
            const container = document.querySelector(".newskycontainer");

            document.body.classList.add("skySpace-background");

            
          }, */
        }
      )
    );

    const controller_Layers_Opacity_True = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const Scene_Layers_Opacity_True = new ScrollMagic.Scene({
      triggerElement: ".skycontainer",
      duration: 200, // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tween_Layers_Opacity_True)
      .addTo(controller_Layers_Opacity_True);

    /* ======================================================================== */

    let tween_Balloon_Path = gsap.timeline({
      scrollTrigger: {
        trigger: ".skycontainer",
        /*  start: "top top", // when the top of the trigger hits the top of the viewport
        end: "bottom top", // end after scrolling 500px beyond the start */
        scrub: 2, // smooth scrubbing, takes 1 second to "catch up" to the scrollbar
        /* markers: true, */
      },
    });

    tween_Balloon_Path.to(".balloon", {
      motionPath: {
        path: [
          { x: 0, y: -50 },
          { x: 0, y: -100 },
          { x: 0, y: -150 },
          { x: 0, y: -200 },
          { x: 0, y: -250 },
          { x: -50, y: -300 },
          { x: -100, y: -350 },
          /*  { x: -200, y: -window.innerHeight }, */
          { x: -window.innerWidth, y: -500 },
        ],
        curviness: 1.25,
        autoRotate: false,
      },
    });

    /* ============================================ */

    let tween_Mountain_Clouds = gsap.timeline({
      // yes, we can add it to an entire timeline!
      scrollTrigger: {
        trigger: ".skycontainer",
        /*  start: "top top", // when the top of the trigger hits the top of the viewport
        end: "bottom top", // end after scrolling 500px beyond the start */
        scrub: 3, // smooth scrubbing, takes 1 second to "catch up" to the scrollbar
        /*  markers: true, */
      },
    });

    tween_Mountain_Clouds.to(".grassOne", {
      transform: "translate(-80%, 10%) translate3d(0px, 0px, 0px) scale(1.5)",
    });
    tween_Mountain_Clouds.to(
      ".grassTwo",
      {
        transform: "translate(80%, 10%) translate3d(0px, 0px, 0px) scale(1.5)",
      },
      "0"
    );
    tween_Mountain_Clouds.to(
      [".cloudOne", ".cloudTwo"],
      {
        transform: "translate(0%, 0%) translate3d(0px, 0px, 0px) scale(1.5)",
      },
      "0"
    );
    /* ======================================= */
    const tween_Layers_Opacity_False = new TimelineLite();

    tween_Layers_Opacity_False.add(
      TweenLite.to(
        [".cloudOne", ".cloudTwo", ".balloon", ".grassOne", ".grassTwo"],
        1,
        {
          opacity: 0,
          /* onComplete: goToNextSection, */
        }
      )
    );

    const controller_Layers_Opacity_False = new ScrollMagic.Controller();

    // Create a ScrollMagic scene
    const Scene_Layers_Opacity_False = new ScrollMagic.Scene({
      triggerElement: ".gap",
      duration: "100%", // Adjust the duration as needed
      triggerHook: 0,
    })
      .setTween(tween_Layers_Opacity_False)
      .setPin(".gap")
      .addTo(controller_Layers_Opacity_False);

    function goToNextSection() {
      // Transition to the next section (e.g., when the plane zoom-in animation is complete)
      const nextSection = document.querySelector(".skill-container");
      window.scrollTo({
        top: nextSection.offsetTop,
        behavior: "smooth",
      });
    }
  },
};
</script>
