<template>
  <div class="block">
      <el-carousel trigger="click" :height="bannerHeight">
        <el-carousel-item v-for="item in banners">
          <a :href="item.link">
            <img :src="item.image" alt="">
          </a>
        </el-carousel-item>
      </el-carousel>
  </div>
</template>

<script>
  export default {
    name: "Carousel",
    props:{
      banners:{
        type:Array,
        default(){
          return []
        }
      },
    },
    data(){
      return{
        bannerHeight:'150px',
        screen:'0px'
      }
    },
    methods:{
      getSize(){
       if(this.screen > 480){
         this.bannerHeight = 300 + 'px'
       }else{
         this.bannerHeight = 150 + 'px'
       }
      }
    },
    mounted() {
      this.screen = window.innerWidth
      this.getSize()
      window.onresize = () => {
        this.screen = window.innerWidth
        this.getSize()
      }
    }
  }
</script>

<style scoped>
  .el-carousel__item img {
    width: 100%;
    height: 100%;
  }
  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
</style>
