<!-- <template>
  <div class="flex flex-row items-stretch w-full pt-20">
    <div
      class="justify-center hidden -mt-[100px] xs:flex xs:w-3/12 md:w-1/4 lg:w-2/5 2xl:w-2/5 3xl:w-5/12"
    >
      <div
        ref="separatorBar"
        class="items-stretch w-5 h-full separatorBar"
      ></div>
      <div
        class="absolute w-12 h-12 cursor-pointer mt-[100px] separatorBox animate-glow"
      >
        <img
          src="../assets/img/ReactIcon.png"
          class="object-contain w-full h-full px-2 py-2"
        />
      </div>
    </div>
    <div class="w-full xs:w-9/12 md:w-full 3xl:-ml-10">
      <h1 class="text-4xl">.Work()</h1>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.box {
  border-radius: 40px;
  background: #151417;
  box-shadow:
    0px 3px 3px 0px #8c5dc9 inset,
    0px 4px 40px 0px #c940eb;
}

.separatorBar {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}

.separatorHorizontalBar {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}
</style>
 -->

<template>
  <div>
    <div class="px-2 editor-tabs">
      <div
        v-for="(tab, index) in tabs"
        :key="index"
        @click="selectTab(index)"
        :class="{ active: activeTab === index }"
      >
        {{ tab }}
      </div>
    </div>
    <div class="code-editor bg-[#24292f]">
      <textarea v-model="currentFileContent" class="bg-[#24292f]"></textarea>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tabs: ["Work.vue", "Work.react"],
      activeTab: 0,
      fileContents: {
        "Work.vue":
          "<template>\n  <div>\n    <!-- Your Vue.js code here -->\n  </div>\n</template>",
        "Work.react":
          'import React from "react";\n\nfunction WorkReact() {\n  // Your React code here\n  return <div></div>;\n}\n\nexport default WorkReact;',
      },
    };
  },
  computed: {
    currentFileContent() {
      return this.fileContents[this.tabs[this.activeTab]];
    },
  },
  methods: {
    selectTab(index) {
      this.activeTab = index;
    },
  },
};
</script>

<style scoped>
.editor-tabs {
  display: flex;
}

.editor-tabs div {
  cursor: pointer;
  padding: 10px;
  background-color: #161b22;
  border: 1px solid #161b22;
  border-bottom: none;
}

.editor-tabs div.active {
  background-color: #24292f;
  border-bottom: 1px solid #161b22;
}

.code-editor {
  border: 1px solid #161b22;
  padding: 10px;
  min-height: 300px;
}

textarea {
  width: 100%;
  height: 100%;
  /* border: none;
    outline: none;
    resize: none; */
}
</style>
