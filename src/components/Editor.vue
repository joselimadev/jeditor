<template>
  <div class="editor">
    <quill-editor
      v-model="content"
      :options="editorOption"
    />
  </div>
</template>

<script>
export default {
  name: "Editor",
  data() {
    return {
      content: "",
      editorOption: {
        modules: {
          toolbar: {
            container: [
              ["bold", "italic", "underline", "strike"],
              ["blockquote", "code-block"],
              [{ header: 1 }, { header: 2 }],
              [{ list: "ordered" }, { list: "bullet" }],
              [{ script: "sub" }, { script: "super" }],
              [{ indent: "-1" }, { indent: "+1" }],
              [{ direction: "rtl" }],
              [{ size: ["small", false, "large", "huge"] }],
              [{ header: [1, 2, 3, 4, 5, 6, false] }],
              [{ font: [] }],
              [{ color: [] }, { background: [] }],
              [{ align: [] }],
              ["emoji"],
              ["clean"],
              ["link", "image", "video"]
            ],
            handlers: { emoji: () => {} }
          },
          imageDrop: true,
          imageResize: {
            modules: ["Resize", "DisplaySize", "Toolbar"]
          },
          "emoji-toolbar": true,
          "emoji-shortname": true
        }
      }
    };
  },
  methods: {}
};
</script>

<style>
.quill-editor,
.quill-code {
  width: 50%;
  height: 90vh;
  margin: auto;
}

.quill-code {
  height: auto;
  border: none;
}

.quill-code > .title {
  border: 1px solid #ccc;
  border-left: none;
  height: 3em;
  line-height: 3em;
  text-indent: 1rem;
  font-weight: bold;
}

.ql-container, .ql-toolbar {
  background-color: #ffffff;
}
</style>
