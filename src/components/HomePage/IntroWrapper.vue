<!--    <div class="flex flex-col border">
          <div class="top-[0%] left-[0%] bg-[#FF8709] rounded-[20px] px-4">
            <h1 class="text-[#131313] text-[80px]">&lt;Template&gt;</h1>
          </div>
          <div class="top-[0%] ml-[4vw] bg-[#FEC5FB] rounded-[20px] px-4">
            <h1 class="text-[#131313] text-[80px]">The begining</h1>
          </div>

          <div class="absolute bottom-[20%] ml-[4vw]">
            <p class="text-[48px] anim pl-[4vw]">
              <span class="text-[#FF8709]">PASSIONATE ABOUT CREATING</span>
              INTERACTIVE APPLICATIONS AND EXPERIENCES ON THE WEB.
            </p>
          </div>
        </div> -->

<!--     <div class="h-[80%] w-[40%] absolute right-0 bottom-0 block">
            <img
              src="../../assets/img/randomobjects.png"
              alt=""
              class="w-[15.375rem]"
            />
          </div> -->
<!--  <div
            class="h-[50%] w-[40%] absolute right-0 bottom-[25%] flex flex-row space-x-10"
          >
            <img
              src="../../assets/img/randomobjects.png"
              alt=""
              class="w-[15.375rem]"
            />
            <img
              src="../../assets/img/randomobjects.png"
              alt=""
              class="w-[15.375rem]"
            />
          </div> -->

<!--  <div class="flex flex-col w-fit">
            <div
              class="bg-[#FF8709] w-fit px-[20px] rounded-[10px] shadow-[4.0px_8.0px_8.0px_rgba(0,0,0,0.38)] z-10"
            >
              <h1 class="text-[#131313] text-[60px]">&lt;Template&gt;</h1>
            </div>

            <div
              class="bg-[#FEC5FB] w-fit ml-[2vw] px-[20px] -mt-1 rounded-[10px] shadow-[4.0px_8.0px_8.0px_rgba(0,0,0,0.38)]"
            >
              <h1 class="text-[#131313] text-[60px]">the beggining...</h1>
            </div>
          </div>

          <div class="absolute bottom-[10%] ml-[2vw] w-1/2">
            <p class="text-[48px] anim">
              <span class="text-[#FF8709]">PASSIONATE ABOUT CREATING</span>
              INTERACTIVE APPLICATIONS AND EXPERIENCES ON THE WEB.
            </p>
          </div> -->

<template>
  <div
    class="wrapperHorizontal relative overflow-x-hidden w-full min-h-screen MichaelAngeloBackground"
  >
    <div
      class="container scrollx flex containerOfthings min-w-fit min-h-screen flex-row items-center justify-center"
    >
      <!-- pt-[14.3rem] pb-[7.5rem] -->

      <!-- First section -->
      <section class="sec1 flex w-[100vw] pt-[14.3rem] pb-[7.5rem] px-[4vw]">
        <div class="w-full relative flex flex-row">
          <div class="flex flex-col w-[50%]">
            <div
              class="bg-[#FF8709] w-fit px-[20px] rounded-[10px] shadow-[4.0px_8.0px_8.0px_rgba(0,0,0,0.38)] z-10"
            >
              <h1 class="text-[#131313] text-[60px]">&lt;Template&gt;</h1>
            </div>

            <div
              class="bg-[#FEC5FB] w-fit ml-[2vw] px-[20px] -mt-1 rounded-[10px] shadow-[4.0px_8.0px_8.0px_rgba(0,0,0,0.38)]"
            >
              <h1 class="text-[#131313] text-[60px]">the beggining...</h1>
            </div>

            <div class="ml-[2vw] mt-40 relative">
              <p class="text-[50px] anim">
                <span class="text-[#FF8709]">PASSIONATE ABOUT CREATING</span>
                INTERACTIVE APPLICATIONS AND EXPERIENCES ON THE WEB.
              </p>
            </div>
          </div>

          <div class="w-[50%] flex flex-row relative">
            <img
              src="../../assets/img/randomobjects.png"
              alt=""
              class="w-96 h-80"
            />
            <img src="../../assets/img/square.png" alt="" class="w-96 h-80" />
            <img src="../../assets/img/quadro.png" alt="" class="w-96 h-80" />
          </div>

          <!-- <div class="h-[50%] w-[40%] relative flex flex-col space-x-10">
            <img src="../../assets/img/randomobjects.png" alt="" class="" />
            <img src="../../assets/img/square.png" alt="" class="" />
            <img src="../../assets/img/quadro.png" alt="" class="" />
          </div> -->
        </div>
      </section>

      <!-- second sec -->
      <section class="sec2 w-fit flex pr-[37vh]">
        <div class="flex items-center will-change-transform">
          <p
            class="home-animate__text-group home-animate__text-group--add text-[200px] anim"
            aria-hidden="true"
          >
            <span>I</span>
            <span>&nbsp;enjoy</span>
            <span>&nbsp;to</span>
            <span class="text-[#131313] bg-[#FF8709] rounded-[30px]"
              >&nbsp;CREATE&nbsp;</span
            >
            <span>THINGS</span>
            <span>&nbsp;THAT</span>
            <span>&nbsp;LIVE</span>
            <span>&nbsp;ON</span>
            <span>&nbsp;THE</span>
            <span>&nbsp;INTERNET</span>
          </p>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    /*  const races = document.querySelector(".containerOfthings");
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
      start: "top 0%",
      end: () => `+=${getScrollAmount() * -0.4}`,
      pin: true,
      animation: tween,
      scrub: 1,
      invalidateOnRefresh: true,
      markers: false,
    }); */

    if (window.innerWidth > 768) {
      const races = document.querySelector(".containerOfthings");

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
        start: "top 0%",
        end: () => `+=${getScrollAmount() * -0.4}`,
        pin: true,
        animation: tween,
        scrub: 1,
        invalidateOnRefresh: true,
        markers: false,
      });
    }
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

.randomobjects {
  /*  bottom: 0;
    right: max(0rem,min(14.7059vw - 11.3971rem,6.25rem));
    width: 15.375rem;
    width: max(26.875rem,min(9.70588vw + 19.3529rem,31rem)); */
  /*   width: 15.375rem; */
}

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
    /*  padding: 20vw 10vw; */
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

.MichaelAngeloBackground {
  /* background-image: url("../../assets/img/WrapperImageOpacity.png");
  background-size: cover; */
}
</style>
