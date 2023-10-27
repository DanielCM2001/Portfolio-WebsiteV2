<template>
  <section>
    <SpaceScene />
    <SkyScene />
  </section>
</template>

<script>
import SpaceScene from "./AnimatedScenes/SpaceScene.vue";
import SkyScene from "./AnimatedScenes/SkyScene.vue";

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
