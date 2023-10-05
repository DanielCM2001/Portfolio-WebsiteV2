<template>
  <div>
    <section
      class="flex items-center justify-center min-h-screen Sky-Background animation"
    >
      <div class="flex flex-col mx-4">
        <p class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)]">
          My interest in Web Development started back in 2017
        </p>
        <p>When I decided to try making a website for a school project</p>
        <p class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)]">
          Turns out making a school project taught me a lot about web
        </p>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  mounted() {
    /*  */
  },
};
</script>

<style scoped>
.animation {
  position: relative;
  height: 100vh;
  overflow: hidden;
}

.Sky-Background {
  background-image: url("../assets/img/Sky.png");
  background-size: cover;
  /*  background-position: center; */
  background-repeat: no-repeat;
}

@keyframes pump {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-20px);
  }
}
</style>
