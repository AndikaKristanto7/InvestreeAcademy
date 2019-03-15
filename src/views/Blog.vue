<template>
  <div class="blog">
    <view-blog-component/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import ViewBlogComponent from '@/components/ViewBlog/ViewBlogComponent.vue';
export default {
  name: 'blog',
  components: {
    // HelloWorld
    ViewBlogComponent
  }
};
</script>
