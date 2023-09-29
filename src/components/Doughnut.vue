<template>
   <Doughnut :data="chartData" :options="chartOptions" />
</template>
<script>
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from 'chart.js'
import { Doughnut } from 'vue-chartjs'

ChartJS.register(ArcElement, Tooltip, Legend)

export default {
  name: 'App',

  data: () => ({

      chartData: {
        labels: ['VueJs', 'EmberJs', 'ReactJs', 'AngularJs'],
        datasets: [
    {
      backgroundColor: ['#41B883', '#E46651', '#00D8FF', '#DD1B16'],
      data: [40, 20, 80, 10]
    }
  ]
      },
      chartOptions: {
        responsive: true
      }
  }),
  components: {
    Doughnut,
  },
};
</script>
<style scoped>

</style>
