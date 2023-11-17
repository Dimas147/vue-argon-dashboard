<template>
  <div class="card">
    <div class="pb-0 card-header mb-0">
      <h6>{{ title }}</h6>
      <p class="text-sm">
        <i class="fa fa-arrow-up text-success"></i>
        <span class="font-weight-bold">{{detail1}}</span>
        {{detail2}}
      </p>
    </div>
    <div class="p-3 card-body">
      <div class="chart">
        <canvas id="chart-line" class="chart-canvas" height="300"></canvas>
      </div>
    </div>
  </div>
</template>

<script>
import Chart from "chart.js/auto";

export default {
  name: "gradient-line-chart",

  props: {
    title: {
      type: String,
      default: "Відстань за рік",
    },
    detail1: {
      type: String,
      default: "+250 км",
    },
    detail2: {
      type: String,
      default: "більше ніж в минулому році",
    },
  },

  mounted() {
    var ctx1 = document.getElementById("chart-line").getContext("2d");

    var gradientStroke1 = ctx1.createLinearGradient(0, 230, 0, 50);

    gradientStroke1.addColorStop(1, "#f5365c");
    gradientStroke1.addColorStop(0, "#5e72e4");
    new Chart(ctx1, {
      type: "bar",
      data: {
        labels: ["Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"],
        datasets: [
          {
            label: "Відстань",
            tension: 0.4,
            borderWidth: 0,
            pointRadius: 0,
            borderColor: "#4BB543 ",
            backgroundColor: gradientStroke1,
            // eslint-disable-next-line no-dupe-keys
            fill: true,
            data: [250, 600, 450, 400, 250, 287, 350, 320, 220],
            maxBarThickness: 50,
          },
        ],
      },
      options: {
        responsive: true,
        maintainAspectRatio: false,
        plugins: {
          legend: {
            display: false,
          },
        },
        interaction: {
          intersect: false,
          mode: "index",
        },
        scales: {
          y: {
            title: {
              display: true,
              text: 'Відстань'
            },
            beginAtZero: true,
            stacked: true,
            grid: {
              drawBorder: true,
              display: true,
              drawOnChartArea: true,
              drawTicks: true,
              borderDash: [10, 10],
            },
            ticks: {
              display: true,
              padding: 10,
              color: "#ccc",
              font: {
                size: 11,
                family: "Open Sans",
                style: "normal",
                lineHeight: 2,
              },
            },
          },
          x: {
            title: {
                display: true,
                text: 'Місяць'
            },
            stacked: true,
            grid: {
              drawBorder: true,
              display: true,
              drawOnChartArea: false,
              drawTicks: true,
              borderDash: [5, 5],
            },
            ticks: {
              display: true,
              color: "#ccc",
              padding: 20,
              font: {
                size: 11,
                family: "Open Sans",
                style: "normal",
                lineHeight: 2,
              },
            },
          },
        },
      },
    });
  },
};
</script>
