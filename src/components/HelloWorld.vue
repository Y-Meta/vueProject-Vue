<template>
  <el-container class="main">
    <el-header height="300">
          <el-carousel indicator-position="none">
            <el-carousel-item v-for="item in carouselList" :key="item.key">
              <img :src="item.src" />
            </el-carousel-item>
          </el-carousel>
    </el-header>
    <el-main>
      <el-container>
        <el-aside>
          <el-timeline>
            <el-timeline-item
              v-for="(activity, index) in activities"
              :key="index"
              :icon="activity.icon"
              :type="activity.type"
              :color="activity.color"
              :size="activity.size"
              :timestamp="activity.timestamp"
            >{{activity.content}}</el-timeline-item>
          </el-timeline>
        </el-aside>
        <el-main></el-main>
      </el-container>
    </el-main>
    <el-footer></el-footer>
  </el-container>
</template>

<script>
  export default {
    data () {
   return {
    carouselList: [
      {key: 'sadas', src: 'https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=1906432669,805384777&fm=26&gp=0.jpg', desc: '111'},
      {key: 'dksaj', src: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1636028025,2351994723&fm=26&gp=0.jpg', desc: '222'}
    ],
     activities: [{
          content: '支持使用图标',
          timestamp: '2018-04-12 20:46',
          size: 'large',
          type: 'primary',
          icon: 'el-icon-more'
        }, {
          content: '支持自定义颜色',
          timestamp: '2018-04-03 20:46',
          color: '#0bbd87'
        }, {
          content: '支持自定义尺寸',
          timestamp: '2018-04-03 20:46',
          size: 'large'
        }, {
          content: '默认样式的节点',
          timestamp: '2018-04-03 20:46'
        }]
    }
  }
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
body {
  margin: 0;
  padding: 0;
}
.el-header {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  line-height: 500px;
}
.el-footer {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #79a2d1;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}

.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
.bg-purple-dark {
  background: #9a60dd;
}
</style>
