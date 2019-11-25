<template>
  <div id="app">
     <h1>Primary editor</h1>
    <vue-editor v-model="content" :editorToolbar="customToolbar"></vue-editor>
    <h1>Non-Editable</h1>
      <div v-html="content" style="min-height:300px;border:1px solid black;"></div>
    <h2>Editable (2 ways)</h2>  
     <vue-editor id="editor2" v-model="content"></vue-editor>
  </div> 
</template>
 
<script>
import { VueEditor } from "vue2-editor";
 
export default {
  components: {
    VueEditor
  },
 
  data() {
    return {
      customToolbar: [[{"header":[false,1,2,3,4,5,6]}],
                      ["bold", "italic", "underline"],
                      [{ "list": "ordered" },{ "list": "bullet" }],
                      ["blockquote","code-block"],
                      ["image"]
                     ],
      content: "<h1>Enthire</h1>"
    };
  }
};
</script>