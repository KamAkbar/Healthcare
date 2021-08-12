<template>
  <section class="chart">
      <h5 class="chart__title">Hospital Survey</h5>
      <AreaChart />
  </section>
</template>

<script>
import AreaChart from './AreaChart.vue'
export default {
    name: 'Chart',
    components: {
        AreaChart
    }
}
</script>

<style lang='scss'>
    .chart{
        background: #FFFFFF;
        box-shadow: 0px 12px 26px rgba(16, 30, 115, 0.06);
        border-radius: 8px;
        padding: 24px;
        margin: 0 32px 38px 31px!important;
        &:hover{
            box-shadow: 12px 0px 24px rgba(16, 30, 115, 0.08);
            transition: .4s;
        }
        &__title{
            font-weight: bold;
            font-size: 20px;
            line-height: 26px;
            letter-spacing: 0.2px;
            color: #25282B;
            text-align: start;
        }
    }
</style>