<template>
<div>
  <nav-bar class="home-nav">
    <div slot="center">商品分类</div>
  </nav-bar>
  <h2>分类</h2>
</div>
</template>

<script>
  import NavBar from "components/common/navbar/NavBar";
  export default {
    name: "Category",
    components:{
      NavBar,
    }
  }
</script>

<style scoped>
  .home-nav{
    background-color:var(--color-tint);
    color: white;
  }
</style>
