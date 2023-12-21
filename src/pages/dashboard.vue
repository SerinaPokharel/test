<script setup lang="ts">
import AnalyticsCongratulations from '@/views/dashboard/AnalyticsCongratulations.vue'
import AnalyticsFinanceTabs from '@/views/dashboard/AnalyticsFinanceTab.vue'
import AnalyticsOrderStatistics from '@/views/dashboard/AnalyticsOrderStatistics.vue'
import AnalyticsProfitReport from '@/views/dashboard/AnalyticsProfitReport.vue'
import AnalyticsTotalRevenue from '@/views/dashboard/AnalyticsTotalRevenue.vue'
import AnalyticsTransactions from '@/views/dashboard/AnalyticsTransactions.vue'

// 👉 Images
import chart from '@images/cards/chart-success.png'
import card from '@images/cards/credit-card-primary.png'
import paypal from '@images/cards/paypal-error.png'
import wallet from '@images/cards/wallet-info.png'
</script>

<template>
  <VRow>

    <VCol
      cols="12"
      md="8"
    >
      <AnalyticsCongratulations />
    </VCol>

    <VCol
      cols="12"
      sm="4"
    >
      <VRow>
        <!-- 👉 payments -->
        <VCol
          cols="12"
          sm="6"
        >
          <CardStatisticsVertical
            v-bind=" {
              title: 'Payments',
              image: paypal,
              stats: 'Rs. 5',
              change: 0,
            }"
          />
        </VCol>

        <!-- 👉 Sales -->
        <VCol
          cols="12"
          md="6"
        >
          <CardStatisticsVertical
            v-bind="{
              title: 'pH Value',
              image: chart,
              stats: '5.6',
              change: 2,
            }"
          />
        </VCol>
      </VRow>
    </VCol>

    <!-- 👉 Total pay -->
    <VCol
      cols="12"
      md="8"
      order="2"
      order-md="1"
    >
      <AnalyticsTotalRevenue />
    </VCol>

    <VCol
      cols="12"
      sm="6"
      md="4"
      order="1"
      order-md="2"
    >
      <VRow>
        <VCol
          cols="12"
          sm="12"
        >
          <AnalyticsProfitReport />
        </VCol>

      </VRow>

      <VRow>
        <VCol
          cols="12"
          sm="12"
          order="3"
        >
          <AnalyticsTransactions />
        </VCol>
      </VRow>
    </VCol>


  </VRow>
</template>
