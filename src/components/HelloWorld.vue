<template>
  <el-carousel indicator-position="outside">
    <el-carousel-item v-for="item in carouselList" :key="item.key">
      <img :src="item.src">
    </el-carousel-item>
  </el-carousel>
</template>

<script>
  export default {
    data () {
   return {
    carouselList: [
      {key: 'sadas', src: 'https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=1906432669,805384777&fm=26&gp=0.jpg', desc: '111'},
      {key: 'dksaj', src: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1636028025,2351994723&fm=26&gp=0.jpg', desc: '222'}
    ]
    }
  }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .el-carousel__item h3 {
    color: #475669;
    font-size: 18px;
    opacity: 0.75;
    line-height: 300px;
    margin: 0;
  }
  
  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }
  
  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
</style>
