<template>
  <div class="home">
    <home-component/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HomeComponent from '@/components/Home/HomeComponent.vue';
export default {
  name: 'home',
  components: {
    // HelloWorld
    HomeComponent
  }
};
</script>
