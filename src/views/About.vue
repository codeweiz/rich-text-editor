<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div id="editor" class="editor"></div>
  </div>
</template>

<script>
import Editor from 'wangeditor'
export default {
  data() {
    return{
      editor: ''
    }
  },
  mounted() {
    this.editor = new Editor('#editor');
    this.editor.custom.uploadImgShowBase64 = true;
    this.editor.custom.showLinkImg = false;
    this.editor.create();
    this.editor.txt.html();
  }
}
</script>
