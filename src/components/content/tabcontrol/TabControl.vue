<template>
  <div class="tab-control">
    <div class="tab-control-item" v-for="(item,index) in titles" :class="{active:currentIndex === index}" @click="changeActive(index)">
      <span>{{item}}</span>
    </div>
  </div>
</template>

<script>
  export default {
    name: "TabControl",
    props:{
      titles:{
        type:Array,
        default(){
          return []
        }
      }
    },
    data(){
      return {
        isActive: false,
        currentIndex: 0
      }
    },
    methods:{
      changeActive(index){
        this.currentIndex = index
      }
    }
  }
</script>

<style scoped>
  .active{
    color: #ff8198;
  }
  .active span{
    border-bottom: 3px solid #ff8198;
    padding: 5px;
  }
  .tab-control{
    display: flex;
    text-align: center;
    font-size: 15px;
    height: 44px;
    line-height: 44px;
  }
  .tab-control-item{
    flex: 1;
  }
</style>
