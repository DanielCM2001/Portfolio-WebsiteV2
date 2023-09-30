<script setup>
import TheNavBar from "../components/TheNavBar.vue";
import Banner from "../components/Banner.vue";
import NewDesignerCoder from "../components/NewDesigner&Coder.vue";
import NewSkills from "../components/NewSkills.vue";
</script>

<template>
  <main>
    <TheNavBar />
    <Banner />
    <NewDesignerCoder />
    <NewSkills />
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
