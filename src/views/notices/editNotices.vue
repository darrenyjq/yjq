<template>
  <div class='tinymce'>
    <editor id='tinymce' v-model='tinymceHtml' :init='init'></editor>
    <div v-html='tinymceHtml'></div>
  </div>
</template>

<script>

import Editor from '@tinymce/tinymce-vue'


export default {
  name: '内容',
  data () {
    return {
      tinymceHtml: '请输入内容',
      init: {
        language_url: '/public/tinymce/zh_CN.js',
        language: 'zh_CN',
        skin_url: '/public/tinymce/skins/lightgray',
        height: 300,
        plugins: 'link lists image code table colorpicker textcolor wordcount contextmenu',
        toolbar:
          'bold italic underline strikethrough | fontsizeselect | forecolor backcolor | alignleft aligncenter alignright alignjustify | bullist numlist | outdent indent blockquote | undo redo | link unlink image code | removeformat',
        branding: false
      }
    }
  },
  mounted () {
    tinymce.init({})
  },
  components: {Editor}
}
</script>






