<template>
    <div>
        <div id="circle"></div>
    </div>
</template>

<script>
export default {
    mounted() {
        let Circle = this.$echarts.init(document.getElementById("circle"))

        Circle.setOption({
            title:{
            left:0,
            backgroundColor:'black',
            borderRadius: [5, 5, 5, 5] ,
            textStyle:{
                color:'white'
            }
        },
    xAxis: {},
    yAxis: {},
    series: [{
        // 点 的大小
        symbolSize: 25,
        // 数据
        data: [
            [10.0, 8.04],
            [8.0, 6.95],
            [13.0, 7.58],
            [9.0, 8.81],
            [11.0, 8.33],
            [14.0, 9.96],
            [6.0, 7.24],
            [4.0, 4.26],
            [12.0, 10.84],
            [7.0, 4.82],
            [5.0, 5.68]
        ],
        // 类型
        type: 'scatter'
    }]
        })
    },
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