<template>
  <div>
    <div class>
      <doughnut-chart
        :data="doughnutChartData"
        :options="doughnutChartOptions"
        :width="60"
        :height="60"
      />
    </div>
  </div>
</template>

<script>
import doughnutChart from "../../plugins/charts/doughnutchart.js";
export default {
  
  components: {
    doughnutChart,
  },

  data: () => ({
    doughnutChartData: {
      labels: ["Cups", "Bags"],
      datasets: [
        {
          label: ["Cups", "Bags"],
          data: [10, 15],
          backgroundColor: ["#DFDFDF", "#F7F7F7"],
        },
      ],
    },
    doughnutChartOptions: {
      responsive: true,
      legend: {
        display: false,
        labels: {
          fontColor: "#263238",
          usePointStyle: true,
        },
      },
      title: {
        display: false,
      },
      cutoutPercentage: 70,
      rotation: Math.PI * 1,
      animation: {
        animateScale: true,
      },
      tooltips: {
        backgroundColor: "#17BF62",
      },
    },
  }),
};
</script>
