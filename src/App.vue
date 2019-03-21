<template lang="html">
  <div class="wrapper">
    <my-header></my-header>
    <!-- <my-content></my-content> -->
    <my-gallery></my-gallery>
  </div>
</template>

<script>
import my_header from './my-header.vue'
//import my_content from './my-content.vue'
import my_gallery from './my-gallery.vue'
export default {
    components:{
        'my-header': my_header,
        // 'my-content': my_content,
        'my-gallery': my_gallery
    }
}
</script>

<style lang="css">
</style>
