<template>
    <div>
        <div id="circle"></div>
    </div>
</template>

<script>
export default {
     mounted() {
    // 获取DOM节点
    let Circle = this.$echarts.init(document.getElementById("circle"));
    // 创建图表
    
    Circle.setOption({
      title: {
        text: '世界人口总量',
        subtext: '数据来自网络'
    },
    tooltip: {
        trigger: 'axis',
        axisPointer: {
            type: 'shadow'
        }
    },
    legend: {
        data: ['2011年', '2012年']
    },
    grid: {
        left: '3%',
        right: '4%',
        bottom: '3%',
        containLabel: true
    },
    xAxis: {
        type: 'value',
        boundaryGap: [0, 0.01]
    },
    yAxis: {
        type: 'category',
        data: ["HTML5", "CSS3", "javascript", "VUE", "NODE"]
    },
    series: [
        {
            name: '2011年',
            type: 'bar',
            data: [70, 34, 60, 78, 69]
        },
        {
            name: '2012年',
            type: 'bar',
            data: [702, 350, 610, 793, 664]
        }
    ]
    });
  }
    
}
</script>

<style>
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