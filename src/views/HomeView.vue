<script setup>
import TheNavBar from "../components/TheNavBar.vue";
import Banner from "../components/Banner.vue";
import DesignerCoder from "../components/DesignerCoder.vue";
import Skills from "../components/Skills.vue";
import VsCodeSimulator from "../components/VsCodeSimulator.vue";
import AboutMyWork from "../components/AboutMyWork.vue";
import Portfolio from "../components/Portfolio.vue";
</script>

<template>
  <main>
    <TheNavBar />
    <Banner />
    <DesignerCoder />
    <Skills />
    <VsCodeSimulator />
    <AboutMyWork />
    <Portfolio />
  </main>
</template>

<script>
export default {
  mounted() {
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        console.log(entry);
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
