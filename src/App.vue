<template>
  <div id="app">
    <header-component/>
    <router-view/>
  </div>
</template>
<script>
  import HeaderComponent from '@/components/Header/HeaderComponent.vue';
  export default {
    components : {
      HeaderComponent
    }
  };
</script>