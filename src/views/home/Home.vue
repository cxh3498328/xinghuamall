<template>
<div id="home">
    <nav-bar class="home-nav">
      <div slot="center">购物街</div>
    </nav-bar>
  <carousel :banners="banners"></carousel>
  <recommend-view :commends="recommends"/>
  <feature-view/>
  <tab-control class="tab-control" :titles="['流行','新款','精选']" />
  <div>
    <ul>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
      <li>列表一</li>
    </ul>
  </div>
</div>
</template>

<script>
  import Carousel from "components/common/carousel/Carousel";
  import NavBar from "components/common/navbar/NavBar"
  import TabControl from "components/content/tabcontrol/TabControl";

  import {getHomeMultidata} from "network/home";

  import FeatureView from "./childComps/FeatureView";
  import RecommendView from "./childComps/RecommendView";


  export default {
    name: "Home",
    data(){
      return {
        banners:[],
        recommends:[],
      }
    },
    components:{
      NavBar,
      Carousel,
      FeatureView,
      RecommendView,
      TabControl,
    },
    created() {
      getHomeMultidata().then(res=>{
        console.log(res);
        this.banners = res.data.banner.list;
        this.recommends = res.data.recommend.list;
      }).catch(err=>{
        console.log(err);
      })
    }
  }
</script>

<style scoped>
  #home{
    padding-top: 44px;
  }
  .home-nav{
    background-color:var(--color-tint);
    color: white;
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    z-index: 9;
  }
  .tab-control{
    position: sticky;
    top:44px;
    background-color: #ffffff;
  }
</style>
