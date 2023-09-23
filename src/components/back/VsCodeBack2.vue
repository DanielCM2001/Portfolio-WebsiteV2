<template>
  <div>
    <div class="tab-buttons">
      <button
        @click="activeTab = 'About.vue'"
        :class="{ active: activeTab === 'About.vue' }"
      >
        About.vue
      </button>
      <button
        @click="activeTab = 'About.react'"
        :class="{ active: activeTab === 'About.react' }"
      >
        About.react
      </button>
    </div>
    <div class="bg-gray-600 tab-content">
      <div v-if="activeTab === 'About.vue'">
        <!-- Code for About.vue -->
        <p>This is the content for About.vue.</p>
      </div>
      <div v-if="activeTab === 'About.react'">
        <!-- Code for About.react -->
        <p>This is the content for About.react.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeTab: "About.vue", // Set the default active tab
    };
  },
};
</script>

<style scoped>
.tab-buttons {
  display: flex;
}

.tab-buttons button {
  background-color: #ccc;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
}

.tab-buttons button.active {
  background-color: #007bff;
  color: #fff;
}

.tab-content {
  margin-top: 10px;
}
</style>
