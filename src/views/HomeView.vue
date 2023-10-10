<script setup>
import Banner from "../components/Banner.vue";
import SpaceAnimated from "../components/SpaceAnimated.vue";
import SkyAnimated from "../components/SkyAnimated.vue";
import NewDesignerCoder from "../components/NewDesigner&Coder.vue";
/* =================== */
import Skills from "../components/Skills.vue";
import EndWrapper from "../components/EndWrapper.vue";
import MadeWithVue from "../components/MadeWith.vue";
import FooterVue from "../components/Footer/Footer.vue";
</script>

<template>
  <main>
    <Banner />
    <SpaceAnimated />
    <SkyAnimated />
    <NewDesignerCoder />
    <!-- =================== -->
    <Skills />
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
