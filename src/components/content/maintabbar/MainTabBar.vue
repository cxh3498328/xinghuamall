<template>
  <tab-bar>
    <tab-bar-item path="/home" >
      <img slot="item-icon-active" src="~assets/img/tabbar/view-active.svg" alt="">
      <img slot="item-icon" src="~assets/img/tabbar/view.svg" alt="">
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category" >
      <img slot="item-icon-active" src="~assets/img/tabbar/list-active.svg" alt="">
      <img slot="item-icon" src="~assets/img/tabbar/list.svg" alt="">
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart" >
      <img slot="item-icon-active" src="~assets/img/tabbar/cart-active.svg" alt="">
      <img slot="item-icon" src="~assets/img/tabbar/cart_empty.svg" alt="">
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile">
      <img slot="item-icon-active" src="~assets/img/tabbar/setting-active.svg" alt="">
      <img slot="item-icon" src="~assets/img/tabbar/setting.svg" alt="">
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </tab-bar>
</template>
<script>
  import TabBar from "components/common/tabbar/TabBar";
  import TabBarItem from "components/common/tabbar/TabBarItem";
  export default {
    name: "MainTabBar",
    components:{
      TabBar,
      TabBarItem,
    }
  }
</script>

<style scoped>

</style>
