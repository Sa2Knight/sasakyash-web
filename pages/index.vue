<template>
  <div class="index">
    <balance-box />
    <div class="columns">
      <div class="column">
        <daily-balance-chart
          title="[公費] 今月の支出状況"
          paymentType="public"
          :monthDateList="[today]"
          :height="500"
        />
      </div>
      <div class="column">
        <daily-balance-chart
          title="[私費] 今月の支出状況"
          paymentType="private"
          :monthDateList="[today]"
          :height="500"
        />
      </div>
    </div>
  </div>
</template>

<script>
import dayjs from 'dayjs'
import dailyBalanceChart from '~/components/commons/dailyBalanceChart'
export default {
  components: { dailyBalanceChart },
  computed: {
    today() {
      return dayjs()
    }
  }
}
</script>

<style lang="scss"></style>
