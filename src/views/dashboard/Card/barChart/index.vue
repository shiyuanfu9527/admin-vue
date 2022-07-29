<template>
<!-- 容器 -->
    <div class="charts" ref="charts">
    </div>
</template>

<script>
// 引入echarts
import * as echarts from 'echarts'
export default {
    name: 'BarChart',

    data() {
        return {
            
        };
    },

    mounted() {
        // 初始化echarts实例
        let lineCharts =echarts.init(this.$refs.charts)
        // 配置数据
        lineCharts.setOption({
            xAxis:{
                show:false,
                type:'category'
            },
            yAxis:{
                show:false
            },
            // 系列
            series:[{
                type:'bar',
                data:[10,7,33,12,48,9,29,10,44,33,22,8],
                color:'cyan'
            }],
            // 布局调试
            grid:{
                left:0,
                top:0,
                bottom:0,
                right:0
            },
            tooltip:{}
        })
    },

    methods: {
        
    },
};
</script>

<style lang="scss" scoped>
.charts{
    width: 100%;
    height: 100%;
}
</style>