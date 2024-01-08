<!-- <template>
  <div
    class="flex items-center justify-center relative min-h-full w-full box-border"
  >
    <div class="wrapperHorizontal relative overflow-x-hidden">
      <div class="container scrollx flex border w-[300vw]">
        <section class="sec1 pin">
          <div class="col border bg-gray-800">
            <p class="text-[48px]">
              <span class="text-[#FF8709]">PASSIONATE ABOUT CREATING</span>
              INTERACTIVE APPLICATIONS AND EXPERIENCES ON THE WEB.
            </p>
          </div>
        </section>

        <section class="sec2 pin">
          <div class="col border bg-gray-900">
            <p class="text-[#FEC5FB] text-[240px]">
              I ENJOY TO CREATE THINGS THAT LIVE ON THE INTERNET
            </p>
          </div>
        </section>
      </div>
    </div>
  </div>
</template> -->

<!-- <template>
  <div class="flex items-center justify-center relative min-h-full w-full">
    <div class="wrapperHorizontal relative overflow-x-hidden">
      <div class="container scrollx flex min-w-max">
        <section class="sec1 pin bg-gray-800 min-w-max">
          <div class="col h-[100vh] flex justify-center items-center min-w-max">
            <p class="text-[48px]">
              <span class="text-[#FF8709]">PASSIONATE ABOUT CREATING</span>
              INTERACTIVE APPLICATIONS AND EXPERIENCES ON THE WEB.
            </p>
          </div>
        </section>

        <section class="sec2 pin whitespace-nowrap min-w-max">
          <div
            class="col h-[100vh] flex justify-center items-center w-max min-w-max"
          >
            <p class="text-[#FEC5FB] text-[240px]">
              I ENJOY TO CREATE THINGS THAT LIVE ON THE INTERNET
            </p>
          </div>
        </section>
      </div>
    </div>
  </div>
</template> -->

<!-- <div class="wrapperHorizontal relative overflow-x-hidden w-full">
    <div class="container scrollx flex">
      <section class="sec1 pin bg-gray-800">
        <div class="col h-[100vh] flex">
          <p class="text-[48px]">
            <span class="text-[#FF8709]">PASSIONATE ABOUT CREATING</span>
            INTERACTIVE APPLICATIONS AND EXPERIENCES ON THE WEB.
          </p>
        </div>
      </section>

      <section class="sec2 pin">
        <div class="col h-[100vh] flex">
          <p class="text-[#FEC5FB] text-[240px]">
            I ENJOY TO CREATE THINGS THAT LIVE ON THE INTERNET
          </p>
        </div>
      </section>
    </div>
  </div> -->
<template>
  <!-- <div
      class="wrapperHorizontal box-border flex relative overflow-x-hidden w-full"
    >
      <div class="container scrollx flex box-border w-[9000px]"> -->

  <div class="wrapperHorizontal relative overflow-x-hidden w-full">
    <div
      class="container scrollx flex w-[8000px] max-w-[9000px] containerOfthings"
    >
      <!-- first sec -->
      <section class="sec1 bg-gray-800 w-[100vw] pb-[7rem] pt-[14rem]">
        <div class="">
          <p class="text-[48px]">
            <span class="text-[#FF8709]">PASSIONATE ABOUT CREATING</span>
            INTERACTIVE APPLICATIONS AND EXPERIENCES ON THE WEB.
          </p>
        </div>
      </section>

      <!-- second sec -->
      <section class="sec2 w-fit flex pr-[37vh]">
        <div class="flex items-center will-change-transform">
          <p
            class="home-animate__text-group home-animate__text-group--add text-[240px]"
            aria-hidden="true"
          >
            <span>I</span>
            <span>&nbsp;ENJOY</span>
            <span>&nbsp;TO</span>
            <span>&nbsp;CREATE</span>
            <span>&nbsp;THINGS&nbsp;</span>
            <span>&nbsp;THAT</span>
            <span>&nbsp;LIVE</span>
            <span>&nbsp;ON</span>
            <span>&nbsp;THE</span>
            <span>&nbsp;INTERNET</span>
          </p>
          <!--   <p class="text-[#FEC5FB] text-[240px]">
              I ENJOY TO CREATE THINGS THAT LIVE ON THE INTERNET
            </p> -->
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    /* ======================================= */

    /* const container = document.querySelector(".container");
    const sections = gsap.utils.toArray(".container section");
    const texts = gsap.utils.toArray(".anim");
    const mask = document.querySelector(".mask");

    let scrollTween = gsap.to(sections, {
      xPercent: -100 * (sections.length - 1),
      ease: "none",
      scrollTrigger: {
        trigger: ".container",
        pin: true,
        scrub: 1,
        end: "+=3000",
        //snap: 1 / (sections.length - 1),
        markers: true,
      },
    });

    console.log(1 / (sections.length - 1));

    //Progress bar animation

    gsap.to(mask, {
      width: "100%",
      scrollTrigger: {
        trigger: ".wrapperHorizontal",
        start: "top left",
        scrub: 1,
      },
    });

    // whizz around the sections
    sections.forEach((section) => {
      // grab the scoped text
      let text = section.querySelectorAll(".anim");

      // bump out if there's no items to animate
      if (text.length === 0) return;

      // do a little stagger
      gsap.from(text, {
        y: -130,
        opacity: 0,
        duration: 2,
        ease: "elastic",
        stagger: 0.1,
        scrollTrigger: {
          trigger: section,
          containerAnimation: scrollTween,
          start: "left center",
          markers: true,
        },
      });
    }); */

    const races = document.querySelector(".containerOfthings");
    console.log(races.offsetWidth);

    function getScrollAmount() {
      let racesWidth = races.scrollWidth;
      return -(racesWidth - window.innerWidth);
    }

    const tween = gsap.to(races, {
      x: getScrollAmount,
      duration: 3,
      ease: "none",
    });

    ScrollTrigger.create({
      trigger: ".wrapperHorizontal",
      start: "top 20%",
      end: () => `+=${getScrollAmount() * -1}`,
      pin: true,
      animation: tween,
      scrub: 1,
      invalidateOnRefresh: true,
      markers: true,
    });
  },
};
</script>

<style>
/* .wrapper {
    overflow-x: hidden;
    position: relative;
  } */
/* * {
    box-sizing: border-box;
  } */

svg {
  position: absolute;
  top: 12em;
  left: 10vw;
  width: 50vw;

  .mask {
    width: 0;
  }
}

.container {
  /*  display: flex;
    width: 300vw; */

  .col {
    /*  display: flex;
      gap: 3em; */

    /*   p {
        font-size: 0.8rem;
      } */
  }

  section {
    /*  width: 100vw; */
    /*  padding: 20vw 10vw; */
    /*    padding: 20vw 10vw; */
    /*  h1 {
        font-size: 3rem;
        margin: 0;
      } */

    p {
      /* font-size: 1.2rem; */
      /* width: 100vw; */
    }

    ul {
      /* list-style-type: none;
        display: flex;
        gap: 3em;
        width: 100%;
        height: 300px;
        padding: 0;
  
        li {
          background: white;
          border-radius: 0.3em;
          flex-grow: 1;
        } */
    }
  }
}

/* section {
    height: 100vh;
  } */
</style>
