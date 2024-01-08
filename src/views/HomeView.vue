<script setup>
import Banner from "../components/HomePage/Banner.vue";
/* import AnimatedScene from "../components/HomePage/AnimatedScene.vue"; */
/* 
import IntroWrapper from "../components/HomePage/IntroWrapper.vue";


import NewDesignerCoder from "../components/HomePage/NewDesigner&Coder.vue";
import Skills from "../components/HomePage/Skills.vue";
import Portfolio from "../components/HomePage/Portfolio.vue";
import EndWrapper from "../components/HomePage/EndWrapper.vue";
import MadeWithVue from "../components/HomePage/MadeWith.vue";
import FooterVue from "../components/Footer/Footer.vue"; */

{
  /* <Banner />
     <IntroWrapper />
  
    <Skills />
    <Portfolio />
     <EndWrapper />
    <MadeWithVue />
    <FooterVue /> */
}
</script>

<template>
  <main><Banner /></main>
</template>

<script>
export default {
  mounted() {
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("show");
        } else {
          entry.target.classList.remove("show");
        }
      });
    });

    const hiddenElements = document.querySelectorAll(".hide");
    hiddenElements.forEach((el) => observer.observe(el));
  },
};
</script>
