<template>
  <div id="app">
 <!--    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->

    <div id="body" class="flex max-w-full">
 
      <div id="sidebar-left" class="flex bg-teal-900 h-screen w-1/5 py-5 justify-center">
        <SidebarMenu/>
      </div>

      <div id="content-main" class="bg-gray-200 w-4/5">
        <router-view/>
      </div>

      
    </div>
    
  </div>


</template>


<script>
  
  import SidebarMenu from '@/components/SidebarMenu';
 
  export default {
    name: 'App',
    components: {
      SidebarMenu
    }
    
  }

</script>


<style lang="scss">

</style>
