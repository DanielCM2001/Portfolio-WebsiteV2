<script setup>
import Banner from "../components/HomePage/Banner.vue";
import AnimatedScene from "../components/HomePage/AnimatedScene.vue";

import SpaceAnimated from "../components/HomePage/SpaceAnimated.vue";
import SkyAnimated from "../components/HomePage/SkyAnimated.vue";
import NewDesignerCoder from "../components/HomePage/NewDesigner&Coder.vue";
import Skills from "../components/HomePage/Skills.vue";
import Portfolio from "../components/HomePage/Portfolio.vue";
import EndWrapper from "../components/HomePage/EndWrapper.vue";
import MadeWithVue from "../components/HomePage/MadeWith.vue";
import FooterVue from "../components/Footer/Footer.vue";
</script>

<template>
  <main>
    <Banner />
     <AnimatedScene /> 
    <Skills />
     <Portfolio />
    <EndWrapper /> 
    <MadeWithVue />
    <FooterVue /> 
  </main>
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
