<template>
  <!-- <div
      class="flex items-center justify-center relative pt-[300px] w-full flex-col"
    >
      <h1 class="text-[#FEC5FB] text-[80px]">&lt;Template&gt;</h1>
      <h1 class="text-[48px]">
        <span class="text-[#FF8709]">PASSIONATE ABOUT CREATING</span> INTERACTIVE
        APPLICATIONS AND EXPERIENCES ON THE WEB.
      </h1>
    </div> -->

  <div
    class="flex items-center justify-center relative min-h-full border w-full"
  >
    <div class="wrapperHorizontal overflow-x-hidden relative">
      <!-- w-[300vw] -->
      <div class="container scrollx flex border w-full">
        <svg
          viewBox="0 0 900 10"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M9.89998 6C9.43671 8.28224 7.41896 10 5 10C2.23858 10 0 7.76142 0 5C0 2.23858 2.23858 0 5 0C7.41896 0 9.43671 1.71776 9.89998 4H445.1C445.563 1.71776 447.581 0 450 0C452.419 0 454.437 1.71776 454.9 4H890.1C890.563 1.71776 892.581 0 895 0C897.761 0 900 2.23858 900 5C900 7.76142 897.761 10 895 10C892.581 10 890.563 8.28224 890.1 6H454.9C454.437 8.28224 452.419 10 450 10C447.581 10 445.563 8.28224 445.1 6H9.89998Z"
            fill="#D9D9D9"
          />
          <mask
            id="mask0_0_1"
            style="mask-type: alpha"
            maskUnits="userSpaceOnUse"
            x="0"
            y="0"
            width="900"
            height="10"
          >
            <path
              d="M9.89998 6C9.43671 8.28224 7.41896 10 5 10C2.23858 10 0 7.76142 0 5C0 2.23858 2.23858 0 5 0C7.41896 0 9.43671 1.71776 9.89998 4H445.1C445.563 1.71776 447.581 0 450 0C452.419 0 454.437 1.71776 454.9 4H890.1C890.563 1.71776 892.581 0 895 0C897.761 0 900 2.23858 900 5C900 7.76142 897.761 10 895 10C892.581 10 890.563 8.28224 890.1 6H454.9C454.437 8.28224 452.419 10 450 10C447.581 10 445.563 8.28224 445.1 6H9.89998Z"
              fill="#D9D9D9"
            />
          </mask>
          <g mask="url(#mask0_0_1)">
            <rect class="mask" y="-49" height="99" fill="black" />
          </g>
        </svg>

        <!-- SECÇÕES -->
        <section class="sec1 pin">
          <h1 class="text-[#FEC5FB] text-[80px]">&lt;Template&gt;</h1>

          <!--  <h1 class="text-[#FEC5FB] text-[60px]">The start...</h1> -->

          <div class="col border">
            <p class="text-[48px] w-[100vw]">
              <span class="text-[#FF8709]">PASSIONATE ABOUT CREATING</span>
              INTERACTIVE APPLICATIONS AND EXPERIENCES ON THE WEB.
            </p>
            <p class="">xd</p>
          </div>
        </section>
        <section class="sec2 pin">
          <!--   <span class="anim">Advanced</span>
            <h1 class="anim">Signify Elegance</h1> -->

          <!-- w-max border overflow-x-auto -->
          <!--  <div class="col anim w-max border overflow-x-auto">
              <p class="text-[#FEC5FB] text-[240px]">
                I ENJOY TO CREATE THINGS THAT LIVE ON THE INTERNET
              </p>
            </div> -->
          <div class="col border">
            <p class="text-[48px] w-[100vw]">
              <span class="text-[#FF8709]">PASSIONATE ABOUT CREATING</span>
              INTERACTIVE APPLICATIONS AND EXPERIENCES ON THE WEB.
            </p>
            <p class="">xd</p>
          </div>
        </section>

        <!-- <section class="sec2 pin">
            <span class="anim">Advanced</span>
            <h1 class="anim">Signify Elegance</h1>
  
            <div class="col anim">
              <p>
                Lorem ipsum dolor sit amet consectetur. Egestas euismod nec sit
                sed massa turpis in. Sit praesent arcu leo lectus pellentesque.
                Ornare elit orci morbi volutpat. Ut fermentum lorem morbi quis
                risus amet urna. Urna egestas lorem.
              </p>
              <p>
                Lorem ipsum dolor sit amet consectetur. Egestas euismod nec sit
                sed massa turpis in. Sit praesent arcu leo lectus pellentesque.
                Ornare elit orci morbi volutpat. Ut fermentum lorem morbi quis
                risus amet urna. Urna egestas lorem.
              </p>
            </div>
          </section>
          <section class="sec3 pin">
            <span class="anim">Advanced</span>
            <h1 class="anim">Signify Elegance</h1>
  
            <div class="col anim">
              <p>
                Lorem ipsum dolor sit amet consectetur. Egestas euismod nec sit
                sed massa turpis in. Sit praesent arcu leo lectus pellentesque.
                Ornare elit orci morbi volutpat. Ut fermentum lorem morbi quis
                risus amet urna. Urna egestas lorem.
              </p>
              <p>
                Lorem ipsum dolor sit amet consectetur. Egestas euismod nec sit
                sed massa turpis in. Sit praesent arcu leo lectus pellentesque.
                Ornare elit orci morbi volutpat. Ut fermentum lorem morbi quis
                risus amet urna. Urna egestas lorem.
              </p>
            </div>
          </section> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    /* ======================================= */

    const container = document.querySelector(".container");
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
  /* display: flex;
    width: 300vw; */

  .col {
    display: flex;
    gap: 3em;

    /*   p {
        font-size: 0.8rem;
      } */
  }

  section {
    /*  width: 100vw;
      padding: 20vw 10vw; */

    padding: 20vw 10vw;

    /*  h1 {
        font-size: 3rem;
        margin: 0;
      } */

    p {
      /* font-size: 1.2rem; */
      /* width: 50vw; */
    }

    ul {
      list-style-type: none;
      display: flex;
      gap: 3em;
      width: 100%;
      height: 300px;
      padding: 0;

      li {
        background: white;
        border-radius: 0.3em;
        flex-grow: 1;
      }
    }
  }
}

/* section {
    height: 100vh;
  } */
</style>
