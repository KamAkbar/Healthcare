<template>
  <section class="container">
      <div class="charts">
          <div class="charts-item">
            <Minichart1 />
          </div>
          <div class="charts-item">
            <Minichart2 />
          </div>
      </div>
  </section>
</template>

<script>
import Minichart1 from './Minichart1.vue'
import Minichart2 from './Minichart2.vue'
export default {
    name: 'Charts',
    components: {
        Minichart1, Minichart2
    }
}
</script>

<style lang="scss">
    .charts{
        display: grid;
        grid-template-columns: 1fr 1fr ;
        grid-gap: 30px;
        margin: 0 32px 30px 31px!important;
        &-item{
            background: #FFFFFF;
            box-shadow: 0px 12px 26px rgba(16, 30, 115, 0.06);
            border-radius: 8px;
            padding: 24px;
            // max-width: 540px;
            &:hover{
                box-shadow: 12px 0px 24px rgba(16, 30, 115, 0.08);
                transition: .4s;
        }
        }
    }
    @media (max-width: 1315px) {
        .charts{
            display: flex!important;
            flex-direction: column;
        }
    }
</style>