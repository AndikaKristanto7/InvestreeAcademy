<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light px-4">
    <a class="navbar-brand" href="#">
      <a id="header-a-logo" href="https://www.investree.id"><img class="site-logo" src="https://www.investree.id/assets/frontend/img/logo.png" alt="Investree"></a>
    </a>
    <a class="navbar-brand" href="https://www.investree.id">
      	<img class="site-logo" src="https://www.investree.id/assets/frontend/img/ojk-indonesia-seeklogo.com-02.png" alt="OJK" style="">
    </a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav ml-auto">    
        <li class="nav-item active" v-for="item in menus">
          <a v-if="item.name == 'Masuk' "class="nav-link" @click="openModal"><button class="btn btn-primary btn-sm">{{ item.name }}</button></a>
          <a v-else-if="item.type === 'button ' "class="nav-link" v-bind:href="item.url" ><button class="btn btn-primary btn-sm">{{ item.name }}</button></a>
          
          <a v-else-if="item.extra_class" class="nav-link" v-bind:class="item.extra_class" :href="item.url">{{ item.name }}</a>
          <a v-else class="nav-link" :href="item.url">{{ item.name }}</a>
        </li>
      </ul>
    </div>
    <login-modal-component :isOpen="isOpen" @close-modal="openModal"/>
  </nav>
</template>

<style>
.navbar {
      background: #FAFAFA;
      padding: 20px 0;
      -webkit-transition: all 0.3s ease-in-out 0s;
      -o-transition: all 0.3s ease-in-out 0s;
      transition: all 0.3s ease-in-out 0s;
      position: fixed;
      width: 100%;
      z-index: 101;
  }
</style>
<script>
// @ is an alias to /src
import LoginModalComponent from '@/components/Modal/LoginModalComponent.vue';
  
export default {
  name: 'HeaderComponent',
  components : {
    LoginModalComponent
  },
  data : function(){
    return {
      menus : [
          {
              name : 'Masuk',
              url : '#',
              type :'button',
          },
          {
              name : 'ID',
              url : '#',
              extra_class : 'border-left',
          },
      ],

    isOpen : false,
    }
  },
  methods: {
        openModal : function(){
          console.log(this.isOpen);
          this.isOpen = !this.isOpen;
      }
    },
};
</script>
