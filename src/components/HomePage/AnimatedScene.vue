<template>
  <section>
    <SpaceScene />
    <SkyScene />
  </section>
</template>

<script>
import SpaceScene from "./AnimatedScenes/SpaceAnimated.vue";
import SkyScene from "./AnimatedScenes/SkyAnimated.vue";

export default {
  setup() {
    return {};
  },
  components: {
    SpaceScene,
    SkyScene,
  },
};
</script>
