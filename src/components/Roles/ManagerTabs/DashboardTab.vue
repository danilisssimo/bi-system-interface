<template>
  <div class="dataset-container">
    <div class="num-cards-container">
      <NumChartCard cardID="num-counter-1" 
        title="Products sold"
        prefix="$"
        footer-suffix="%"
        :footer-display-prefix="true" 
        :value="dashboardData.soldProducts.sold_amount" 
        :footer-value="dashboardData.soldProducts.diff_from_last_month"
        :footer-is-toogle-up="dashboardData.soldProducts.diff_from_last_month < 0" 
        :description="dashboardData.soldProducts.description">
      </NumChartCard>
      <NumChartCard cardID="num-counter-2" 
        title="Sales plan"
        prefix="$" 
        :value="dashboardData.salesPlan.sales_amount"
        :footer-value="dashboardData.salesPlan.completed_precent"
        footer-suffix="%"
        :footer-display-prefix="false" 
        :footer-is-reverse="true" 
        description="completed on">
      </NumChartCard>
      <NumChartCard cardID="num-counter-3" 
        title="My efficiency" 
        suffix="%"
        footer-suffix="%"
        :footer-display-prefix="true"
        :value="dashboardData.efficiency.current"
        :footer-value="dashboardData.efficiency.diff_from_last_month"
        :description="dashboardData.efficiency.description">
      </NumChartCard>
      <NumChartCard cardID="num-counter-4"
        title="My new customers"
        footer-suffix="%"
        :footer-display-prefix="true"
        :value="dashboardData.newCustomers.amount"
        :footer-value="dashboardData.newCustomers.diff_from_last_month"
        :description="dashboardData.newCustomers.description">
      </NumChartCard>
    </div>
    <div class="data-container">
      <PieChartCard cardID="pie-chart-1" 
        title="My revenue" 
        :value="dashboardData.userRevenue.value"
        :labels="['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange']" 
        :data="[11, 9, 13, 25, 21, 15]"
        :footer-value="46.9" 
        footer-description="more than last month" 
        prefix="$">
      </PieChartCard>
      <RadarChartCard cardID="radar-chart-1" title="KPI Execution" :data="[0, 0.4, 0.2, 0.1, 0.6, 0.9]"
        :labels="['Eating', 'Drinking', 'Sleeping', 'Coding', 'Cycling', 'Running']">
      </RadarChartCard>
    </div>
  </div>
  <div class="dataset-container">
    <div class="data-container">
      <LineChartCard cardID="line-chart-1" title="Sales dynamics"
        :labels="['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']"
        :datasets="[
          { label: 'Dataset 1', data: [12, 15, 21, 10, 16, 11, 20, 22, 18, 17, 14, 13], tension: 0.3 },
          { label: 'Dataset 2', data: [11, 16, 20, 10, 15, 10, 21, 24, 15, 10, 18, 11], tension: 0.3 }
        ]">
      </LineChartCard>
      <PhotoCard title="Most popular" 
        value="Tesla Model S"
        photo-url="https://digitalassets.tesla.com/tesla-contents/image/upload/f_auto,q_auto/Mega-Menu-Vehicles-Model-S.png">
      </PhotoCard>
    </div>
  </div>
  <div class="dataset-container" style="overflow: hidden;">
    <TableCard :columns="[
      { key: 'client', value: 'Client' },
      { key: 'reg_date', value: 'Registration date' },
      { key: 'sale_date', value: 'Sale date' },
      { key: 'product_name', value: 'Product name' },
      { key: 'sale_amount', value: 'Sale amount' }
    ]" :data="[
          {
            'client': {'type':'text', 'data':'Name Surename'},
            'reg_date': {'type':'text', 'data':'10.11.2024'},
            'sale_date': {'type':'text', 'data':'10.15.2024'},
            'product_name': {'type':'text', 'data':'Tesla Model S'},
            'sale_amount': {'type':'text', 'data':'$ 20244'},
          }, {
            'client': {'type':'text', 'data':'Name Surename'},
            'reg_date': {'type':'text', 'data':'10.11.2024'},
            'sale_date': {'type':'text', 'data':'10.15.2024'},
            'product_name': {'type':'text', 'data':'Tesla Model S'},
            'sale_amount': {'type':'text', 'data':'$ 20244'},
          },{
            'client': {'type':'text', 'data':'Name Surename'},
            'reg_date': {'type':'text', 'data':'10.11.2024'},
            'sale_date': {'type':'text', 'data':'10.15.2024'},
            'product_name': {'type':'text', 'data':'Tesla Model S'},
            'sale_amount': {'type':'text', 'data':'$ 20244'},
          },{
            'client': {'type':'text', 'data':'Name Surename'},
            'reg_date': {'type':'text', 'data':'10.11.2024'},
            'sale_date': {'type':'text', 'data':'10.15.2024'},
            'product_name': {'type':'text', 'data':'Tesla Model S'},
            'sale_amount': {'type':'text', 'data':'$ 20244'},
          },{
            'client': {'type':'text', 'data':'Name Surename'},
            'reg_date': {'type':'text', 'data':'10.11.2024'},
            'sale_date': {'type':'text', 'data':'10.15.2024'},
            'product_name': {'type':'text', 'data':'Tesla Model S'},
            'sale_amount': {'type':'text', 'data':'$ 20244'},
          },{
            'client': {'type':'text', 'data':'Name Surename'},
            'reg_date': {'type':'text', 'data':'10.11.2024'},
            'sale_date': {'type':'text', 'data':'10.15.2024'},
            'product_name': {'type':'text', 'data':'Tesla Model S'},
            'sale_amount': {'type':'text', 'data':'$ 20244'},
          },{
            'client': {'type':'text', 'data':'Name Surename'},
            'reg_date': {'type':'text', 'data':'10.11.2024'},
            'sale_date': {'type':'text', 'data':'10.15.2024'},
            'product_name': {'type':'text', 'data':'Tesla Model S'},
            'sale_amount': {'type':'text', 'data':'$ 20244'},
          },{
            'client': {'type':'text', 'data':'Name Surename'},
            'reg_date': {'type':'text', 'data':'10.11.2024'},
            'sale_date': {'type':'text', 'data':'10.15.2024'},
            'product_name': {'type':'text', 'data':'Tesla Model S'},
            'sale_amount': {'type':'text', 'data':'$ 20244'},
          },{
            'client': {'type':'text', 'data':'Name Surename'},
            'reg_date': {'type':'text', 'data':'10.11.2024'},
            'sale_date': {'type':'text', 'data':'10.15.2024'},
            'product_name': {'type':'text', 'data':'Tesla Model S'},
            'sale_amount': {'type':'text', 'data':'$ 20244'},
          },{
            'client': {'type':'text', 'data':'Name Surename'},
            'reg_date': {'type':'text', 'data':'10.11.2024'},
            'sale_date': {'type':'text', 'data':'10.15.2024'},
            'product_name': {'type':'text', 'data':'Tesla Model S'},
            'sale_amount': {'type':'text', 'data':'$ 20244'},
          },
        ]"></TableCard>
  </div>
</template>

<script>
import PhotoCard from '@/components/Metrics/PhotoCard.vue';
import PieChartCard from '@/components/Metrics/PieChartCard.vue';
import LineChartCard from '@/components/Metrics/LineChartCard.vue';
import RadarChartCard from '@/components/Metrics/RadarChartCard.vue';
import NumChartCard from '@/components/Metrics/NumChartCard.vue';
import TableCard from '@/components/Metrics/TableCard.vue';

export default {
  name: "DashboardTab",
  data() {
    return {
      dashboardData: {
        "soldProducts": {
          "sold_amount": 53245, 
          "diff_from_last_month": -12.23, 
          "description": "more then last month"
        },
        "salesPlan": { 
          "sales_amount": 523245,
          "completed_precent": 43,
          "new_clients": null 
        },
        "efficiency": {
          "current": 73,
          "diff_from_last_month": 72,
          "description": "more then last month"
        },
        "newCustomers": {
          "amount": 57,
          "diff_from_last_month": -18.1,
          "description": "more than last month"
        },
        "userRevenue": {
          "value": 23913,
          "labels": [],
          "datasets": []
        },
        "userKPI": null
      }
    }
  },
  components: {
    PieChartCard, LineChartCard, RadarChartCard, NumChartCard, TableCard, PhotoCard
  }
}
</script>

<style scoped>
@import url(/src/assets/styles/index.css);
</style>