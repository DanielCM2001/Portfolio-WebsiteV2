<template>
  <div
    class="flex items-center justify-center w-full skill-container min-h-screen"
  >
    <div
      class="w-full md:w-full mx-[4vw] justify-center items-center flex flex-col"
    >
      <h1
        class="text-[12.5vw] xs:text-[50px] md:text-[80px] xl:text-[110px] 2xl:text-[120px] text-[#F5EEE6]"
      >
        LATEST WORK
      </h1>

      <h1
        class="text-[12.5vw] xs:text-[50px] md:text-[80px] xl:text-[110px] 2xl:text-[120px] text-[#F5EEE6]"
      >
        SOME OF MY PROJECTS...
      </h1>

      <div class="w-full flex flex-col">
        <hr class="w-full border-b-2 my-5" />
        <div
          class="flex flex-row w-full justify-evenly text-[40px] link relative"
        >
          <h1>LOREM IPSUM</h1>
          <h1>Development, Design</h1>
          <h1>2023</h1>
          <div class="hover-reveal image01">
            <img
              src="../../assets/img/1.png"
              class="hidden-img z-10 mix-blend-difference"
              alt=""
            />
          </div>
        </div>
        <hr class="w-full border-b-2 my-5" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  mounted() {
    /* const link = document.querySelectorAll(".link");
    const hoverReveal = document.querySelectorAll(".hover-reveal");
    const linkImages = document.querySelectorAll(".hidden-img");

    for (var i = 0; i < link.length; i++) {
      link[i].addEventListener("mousemove", (e) => {
        hoverReveal[i].style.opacity = 1;
        hoverReveal[i].style.transform = `translate(-100%,-50%) rotate(5deg)`;
        linkImages[i].style.transform = "scale(1,1)";
        hoverReveal[i].style.left = e.clientX + "px";
      });
      link[i].addEventListener("mouseleave", (e) => {
        hoverReveal[i].style.opacity = 0;
        hoverReveal[i].style.transform = `translate(-50%,-50%) rotate(-5deg)`;
        linkImages[i].style.transform = "scale(0.8,0.8)";
      });
    } */
  },
};
</script>

<style scoped>
/* .hover-reveal {
  position: absolute;
  width: 300px;
  height: 400px;
  top: 50%;
  left: 50%;
  pointer-events: none;
  transform: translate(-50%, -50%);
  overflow: hidden;
  opacity: 0;
  transform: scale(0.8);
  transition: all 0.5s ease-out;
}

.hover-reveal img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: relative;
  transition: text-transform 0.5s ease-out;
} */

.link img {
  position: absolute;
  width: 300px;
  height: 400px;
  top: 50%;
  left: 50%;
  pointer-events: none;
  transform: translate(-100%, -50%) rotate(5deg);
  overflow: hidden;
  opacity: 0;
  transform: scale(0.8);
  transition: all 0.5s ease-out;
}

.link:hover img {
  /*  width: 100%;
  height: 100%; */
  transform: translate(-50%, -50%) rotate(-5deg);
  object-fit: cover;
  position: absolute;

  opacity: 1;
  transition: text-transform 0.5s ease-out;
}
</style>
