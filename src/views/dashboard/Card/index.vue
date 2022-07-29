<template>
  <div>
    <el-row :gutter="10">
      <el-col :span="6">
        <el-card >
          <Detail title="总销售额" count='￥ 126560'>
            <template slot='charts'>
                <span>周同比&nbsp;&nbsp;56.67%<svg t="1658949090967" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2171" width="16" height="16"><path d="M698.7 480.9v429.5c0 54.8-44.5 99.3-99.3 99.3H434c-54.8 0-99.3-44.5-99.3-99.3V480.9H70l446.9-463 446.9 463H698.7z m0 0" fill="#d81e06" p-id="2172"></path></svg></span>
                &nbsp;&nbsp;
                <span>日同比&nbsp;&nbsp;19.96%<svg t="1658949172023" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="3364" width="16" height="16"><path d="M258.048 568.832l253.952 279.04 253.952-279.04c22.016-24.064 13.312-43.52-18.944-43.52H629.76v-322.56c0-32.768-26.112-58.88-58.88-58.88h-117.76c-32.256 0-58.368 26.112-58.88 58.368v323.072H276.992c-31.744 0-40.448 19.456-18.944 43.52z" fill="#1afa29" p-id="3365"></path></svg></span>
            </template>
            <template slot='footer'>
                <span>日销售额￥12423</span>
            </template>
          </Detail>
        </el-card>
      </el-col>
      <el-col :span="6">
        <el-card >
          <Detail title="访问量" count='88460'>
            <template slot="charts">
              <LineChart></LineChart>
            </template>
             <template slot='footer'>
                <span>日访问量 1234</span>
            </template>
          </Detail>
        </el-card>
      </el-col>
      <el-col :span="6">
        <el-card >
          <Detail title="支付笔数" count='88460'>
            <template slot="charts">
              <BarChart></BarChart>
            </template>
             <template slot='footer'>
                <span>转换率64%</span>
            </template>
          </Detail>
        </el-card>
      </el-col>
      <el-col :span="6"
        ><el-card >
          <Detail title="运营活动效果" count='78'>
            <template slot="charts">
              <ProgressChart></ProgressChart>
            </template>
             <template slot='footer'>
<span>周同比&nbsp;&nbsp;56.67%<svg t="1658949090967" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2171" width="16" height="16"><path d="M698.7 480.9v429.5c0 54.8-44.5 99.3-99.3 99.3H434c-54.8 0-99.3-44.5-99.3-99.3V480.9H70l446.9-463 446.9 463H698.7z m0 0" fill="#d81e06" p-id="2172"></path></svg></span>
                &nbsp;&nbsp;
                <span>日同比&nbsp;&nbsp;19.96%<svg t="1658949172023" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="3364" width="16" height="16"><path d="M258.048 568.832l253.952 279.04 253.952-279.04c22.016-24.064 13.312-43.52-18.944-43.52H629.76v-322.56c0-32.768-26.112-58.88-58.88-58.88h-117.76c-32.256 0-58.368 26.112-58.88 58.368v323.072H276.992c-31.744 0-40.448 19.456-18.944 43.52z" fill="#1afa29" p-id="3365"></path></svg></span>
            </template></Detail> </el-card
      ></el-col>
    </el-row>
  </div>
</template>

<script>
import Detail from "./Detail";
import LineChart from './lineChart'
import BarChart from './barChart'
import ProgressChart from './progressChart'
export default {
  name: "card",
  components: {
    Detail,
    LineChart,
    BarChart,
    ProgressChart
  },
};
</script>

<style lang="scss" scoped>
.el-row{
    .el-col{
        .el-card{
            margin:10px 5px
        }
    }
}
</style>