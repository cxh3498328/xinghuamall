<template>
  <div class="recommend">
    <div class="commend" v-for="item in commends">
      <a :href="item.link">
        <img :src="item.image">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
  export default {
    name: "RecommendView",
    props:{
      commends:{
        type:Array,
        default(){
          return []
        }
      },
    }
  }
</script>

<style scoped>
  .recommend{
    width: 100%;
    display: flex;
    text-align: center;
    padding: 15px 0 20px;
    border-bottom: 8px solid #eee;
  }
  .commend{
    flex: 1;
    font-size: 12px;
  }
  .commend img{
    width: 70px;
    height: 70px;
    margin-bottom: 10px;
  }
</style>
