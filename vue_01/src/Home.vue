<template>
  <div class="home">
    <div id="circle">
      <div class="img"></div>
    </div>
  </div>
</template>

<script>

export default {
  name: "Home",
  components: {

  },
  mounted() {
    // 获取DOM节点
    let Circle = this.$echarts.init(document.getElementById("circle"));
    // 创建图表
    Circle.setOption({
      color: ['#3398DB'],
    tooltip: {
        trigger: 'axis',
        axisPointer: {            // 坐标轴指示器，坐标轴触发有效
            type: 'shadow'        // 默认为直线，可选为：'line' | 'shadow'
        }
    },
    grid: {
        left: '0%',
        top:"10px",
        right: '0%',
        bottom: '4%',
        containLabel: true
    },
    xAxis: [
        {
            type: 'category',
            data: [
                "旅游行业",
                "教育培训",
                "游戏行业",
                "医疗行业",
                "电商行业",
                "社交行业",
                "金融行业"],
            axisTick: {
                alignWithLabel: true
            },
            axisLabel: {
              textStyle: {
                color: "black",
                fontSize: "12"
              }
            },
            axisLine: {
            show: false
        }
        }
    ],
    yAxis: [
        {
            type: 'value',
            axisLabel: {
            textStyle: {
            color: "black" ,
            fontSize: "12"
          }
            },
            axisLine: {
          lineStyle: {
            color: "black"
            // width: 1,
            // type: "solid"
          }
        },
        splitLine: {
          lineStyle: {
            color: "black"
            }
          }
        }
    ],
    series: [
        {
            name: '直接访问',
            type: 'bar',
            barWidth: '35%',
            data: [200, 300, 300, 900, 1500, 1200, 600],
            itemStyle: {
          barBorderRadius: 5
        }
        }
    ]
    });
  }
};
</script>

<style scoped>
#circle {
  width: 600px;
  height: 600px;
  background: yellowgreen;
  display: flex;
  justify-content: center;
  align-items: center;
  margin:  0 auto;
}
</style>