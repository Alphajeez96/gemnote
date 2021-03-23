<template>
  <div>
    <barChart :data="chartdata" :options="options" :height="120" />
  </div>
</template>

<script>
import barChart from "../../plugins/charts/barchart.js";

export default {
  components: {
    barChart,
  },

  data: () => ({
    
    chartdata: {
      labels: [
        "Jan",
        "Feb",
        "Mar",
        "Apr",
        "May",
        "Jun",
        "Jul",
        "Aug",
        "Sep",
        "Oct",
        "Nov",
        "Dec",
      ],

      datasets: [
        {
          data: [65, 40, 55, 70, 50, 50, 50, 55, 70, 55, 40, 45, 8],
          backgroundColor: "#DFDFDF",
          borderColor: "#DFDFDF",
          borderWidth: 1,
        },
      ],
    },
    options: {
      responsive: true,
      maintainAspectRatio: true,
      showLine: true,
      legend: {
        display: false,
      },
      scales: {
        xAxes: [
          {
            barPercentage: 0.6,
            gridLines: {
              display: false,
            },
            ticks: {
              fontSize: 12,
              fontColor: " #878B9A",
            },
          },
        ],
        yAxes: [
          {
            gridLines: {
              borderDash: [5, 2],
              color: "#E6E8E8",
              display: true,
            },
            ticks: {
              fontSize: 12,
              fontColor: " #878B9A",
            },
          },
        ],
      },
    },
  }),
};
</script>

