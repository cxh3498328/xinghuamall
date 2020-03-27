<template>
  <div id="app">
    <main-tab-bar/>
    <router-view></router-view>
  </div>
</template>
<script>
  require('assets/css/base.css')
  import MainTabBar from 'components/content/maintabbar/MainTabBar'
  export default {
    name:'app',
    components:{
      MainTabBar,
    }
  }
</script>
<style>
</style>
