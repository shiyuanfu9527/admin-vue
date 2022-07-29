<template>
  <div>
    <div class="header">
      <span class="search-header">搜索用户数</span>
      <svg
        t="1658948348024"
        class="icon"
        viewBox="0 0 1024 1024"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        p-id="2225"
        width="26"
        height="26"
      >
        <path
          d="M512 64C264.6 64 64 264.6 64 512s200.6 448 448 448 448-200.6 448-448S759.4 64 512 64z m0 820c-205.4 0-372-166.6-372-372s166.6-372 372-372 372 166.6 372 372-166.6 372-372 372z"
          p-id="2226"
          fill="#707070"
        ></path>
        <path
          d="M512 336m-48 0a48 48 0 1 0 96 0 48 48 0 1 0-96 0Z"
          p-id="2227"
          fill="#707070"
        ></path>
        <path
          d="M536 448h-48c-4.4 0-8 3.6-8 8v272c0 4.4 3.6 8 8 8h48c4.4 0 8-3.6 8-8V456c0-4.4-3.6-8-8-8z"
          p-id="2228"
          fill="#707070"
        ></path>
      </svg>
    </div>
    <div class="main">
      <span class="main-title">12321</span>
      <span class="main-content">17.1</span>
      <svg
        t="1658949090967"
        class="icon"
        viewBox="0 0 1024 1024"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        p-id="2171"
        width="16"
        height="16"
      >
        <path
          d="M698.7 480.9v429.5c0 54.8-44.5 99.3-99.3 99.3H434c-54.8 0-99.3-44.5-99.3-99.3V480.9H70l446.9-463 446.9 463H698.7z m0 0"
          fill="#d81e06"
          p-id="2172"
        ></path>
      </svg>
      <svg
        t="1658949172023"
        class="icon"
        viewBox="0 0 1024 1024"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        p-id="3364"
        width="20"
        height="20"
      >
        <path
          d="M258.048 568.832l253.952 279.04 253.952-279.04c22.016-24.064 13.312-43.52-18.944-43.52H629.76v-322.56c0-32.768-26.112-58.88-58.88-58.88h-117.76c-32.256 0-58.368 26.112-58.88 58.368v323.072H276.992c-31.744 0-40.448 19.456-18.944 43.52z"
          fill="#1afa29"
          p-id="3365"
        ></path>
      </svg>
    </div>
    <div class="footer">
      <div class="charts" ref="charts"></div>
    </div>
  </div>
</template>

<script>
import * as echarts from 'echarts'
export default {
  name: "LineCharts",

  data() {
    return {};
  },

  mounted() {
    // 初始化echarts实例
    let lineCharts = echarts.init(this.$refs.charts);
    // 配置数据
    lineCharts.setOption({
      xAxis: {
        show: false,
        type: "category",
      },
      yAxis: {
        show: false,
      },
      // 系列
      series: [
        {
          type: "line",
          smooth: true,
          data: [10, 7, 33, 12, 48, 9, 29, 10, 44],
          // 拐点的样式的设置
          itemStyle: {
            opacity: 0,
          }, //线条的样式
          lineStyle: {
            color: "blue",
          },
          // 填充颜色设置
          areaStyle: {
            color: {
              type: "linear",
              x: 0,
              y: 0,
              x2: 0,
              y2: 1,
              colorStops: [
                {
                  offset: 0,
                  color: "blue", //0%处的颜色
                },
                {
                  offset: 1,
                  color: "#fff", //100%处的颜色
                },
              ],
              global: false, //缺省为false
            },
          },
        },
      ],
      // 布局调试
      grid: {
        left: 0,
        top: 0,
        bottom: 0,
        right: 0,
      },
    });
  },
}
</script>

<style lang="scss" >
.header {
  display: flex;
  align-items: center;
}
.search-header {
  margin-right: 20px;
}
.main-title {
  margin-right: 30px;
}
.main {
  margin: 10px 0;
}
.main-content {
  margin-right: 10px;
}
.charts {
  width: 100%;
  height: 50px;
}
</style>