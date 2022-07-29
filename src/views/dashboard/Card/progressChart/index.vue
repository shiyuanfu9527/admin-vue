<template>
<!-- 容器 -->
    <div class="charts" ref="charts">
    </div>
</template>

<script>
// 引入echarts
import * as echarts from 'echarts'
export default {
    name: 'ProgressChart',

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
                // 最小值与最大值的设置
                min:0,
                max:100
            },
            yAxis:{
                show:false,
                // 均分
                type:'category'
            },
            // 系列
            series:[{
                type:'bar',
                data:[78],
                //柱状图的宽度
                barWidth:10,
                color:'yellowgreen',
                showBackground:true,
                // 设置背景颜色
                backgroundStyle:{
                    color:'#eee'
                },
                // 文本标签
                label:{
                    show:true,
                    // 改变样式
                    formatter:'|',
                    // 文本标签位置调试
                    position:'right'
                }

            }],
            // 布局调试
            grid:{
                left:0,
                top:0,
                bottom:0,
                right:0
            }
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