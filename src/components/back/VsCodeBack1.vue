<template>
  <div class="flex flex-col w-3/4 vscode-simulator">
    <div class="flex flex-row px-1 space-x-5 bg-[#161b22] file-tabs">
      <div
        v-for="(file, index) in files"
        :key="index"
        @click="selectFile(index)"
        :class="{ active: activeFileIndex === index }"
        class="flex items-center px-5 py-2 mt-2"
      >
        <img :src="file.src" class="w-4 h-3 mr-3" />
        {{ file.name }}
      </div>
    </div>
    <div class="editor-container">
      <div class="line-numbers">
        <pre>{{ lineNumbers }}</pre>
      </div>
      <div class="code-editor">
        <pre
          contenteditable="false"
          @input="updateCode"
          :class="{ highlighted: isHighlighted }"
        >
            {{ code }}
          </pre
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      files: [
        {
          name: "Work.Vue",
          code: "<template> const \n  <div>\n    <!-- Your Vue.js code here -->\n  </div>\n</template>",
          src: new URL(`@/assets/img/VueIcon.png`, import.meta.url),
        },
        {
          name: "Work.React",
          code: 'import React from "react";\n\nfunction WorkReact() {\n  // Your React code here\n  return <div></div>;\n}\n\nexport default WorkReact;',
          src: new URL(`@/assets/img/ReactIcon.png`, import.meta.url),
        },
      ],
      activeFileIndex: 0,
      isHighlighted: false,
    };
  },
  computed: {
    code() {
      return this.files[this.activeFileIndex].code;
    },
    lineNumbers() {
      const lines = this.code.split("\n");
      return lines.map((_, index) => index + 1).join("\n");
    },
  },
  methods: {
    selectFile(index) {
      this.activeFileIndex = index;
    },
    updateCode(event) {
      this.files[this.activeFileIndex].code = event.target.innerText;
    },
  },
};
</script>

<style scoped>
/* Add your styles for the VS Code simulator here */
.vscode-simulator {
  display: flex;
  font-family: "Consolas", "Courier New", monospace;
}

.editor-container {
  display: flex;
  background-color: #161b22;
  color: #d4d4d4;
  border: 2px solid #30363d;
}

.line-numbers {
  background-color: #24292f;
  color: #959e9e;
  padding: 10px;
  white-space: pre-wrap;
}

.line-numbers pre {
  user-select: none;
}

.code-editor {
  flex-grow: 1;
  padding: 10px;
  overflow: auto;
  background-color: #24292f;
  min-width: 0;
}

.code-editor pre {
  margin: 0;
  white-space: pre-wrap;
}

.code-editor .highlighted {
  color: #c586c0; /* Purple for variable names */
}

.file-tabs div {
  cursor: pointer;
  background-color: #161b22;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;

  /*  border-radius: 1px; */
  /*   border: 1px solid #ddd;
    border-bottom: none; */
}

.file-tabs div.active {
  background-color: #24292f;
  /* border-bottom: 1px solid #30363d; */
}
</style>
