<template>
  <div id="app">
    <!--创建一个echarts的容器-->
    <div id="main" :style="{width: '300px', height: '300px'}"></div>
    
  </div>
  
</template>
<script>
    export default {
  name: 'FuncFormsBase',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  mounted () {
    this.drawLine();
  },
  methods: {
    drawLine () {
      var echarts = require('echarts');
      var myChart = echarts.init(document.getElementById('main'));
      myChart.setOption({
         angleAxis: {
    },
    radiusAxis: {
        type: 'category',
        data: ['周一', '周二', '周三', '周四'],
        z: 10
    },
    polar: {
    },
    series: [{
        type: 'bar',
        data: [1, 2, 3, 4],
        coordinateSystem: 'polar',
        name: 'A',
        stack: 'a'
    }, {
        type: 'bar',
        data: [2, 4, 6, 8],
        coordinateSystem: 'polar',
        name: 'B',
        stack: 'a'
    }, {
        type: 'bar',
        data: [1, 2, 3, 4],
        coordinateSystem: 'polar',
        name: 'C',
        stack: 'a'
    }],
    legend: {
        show: true,
        data: ['A', 'B', 'C']
    }
      });
    }
  }
}
</script>