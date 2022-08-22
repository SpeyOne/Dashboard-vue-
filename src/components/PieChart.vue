<template>
  <div class="pie_chart">
    <p><strong>Client Hours</strong><br />Working Hours</p>
    <div class="piechart">
      <apexchart
        type="donut"
        :options="chartOptions"
        :series="series"
      ></apexchart>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      series: [35, 26, 35],
      chart: {
        type: "donut",
        size: 350,
      },
      chartOptions: {
        labels: [
          "Sweet & Simple LTD. 37:45 h",
          "Nike Running Shoes 16:22 h",
          "Some Cool Company 3:14 h",
        ],
        colors: ["#ff4081", "#f50057", "#ff80ab"],
        chart: {
          id: "vuechart-example",
          toolbar: {
            show: false,
          },
        },

        dataLabels: {
          enabled: false,
        },
        legend: {
          show: true,
          colors: ["#ff80ab", "#f50057", "#ff4081"],
          position: "bottom",
          horizontalAlign: "left",
          offsetX: -10,
          width: 320,
          markers: {
            width: 10,
            height: 10,
            fillColors: ["#ff4081", "#f50057", "#ff80ab"],
          },
        },
      },
    };
  },
};
</script>

<style>
.pie_chart {
 font-family: "Avenir Next Cyr", sans-serif;
 width: 315px;
 height: 500px;
 background-color: #ffffff;
 margin-right: 10px;
 margin-left: 300px;
 border: 1px solid #f2f3f3;
}

.pie_chart p {
 margin: 20px 0 0 15px;
 font-size: 13px;
 color: #78909c;
 line-height: 20px;
 text-align: left;
}

.pie_chart strong {
 font-size: 21px;
 color: #37474f;
 font-weight: normal;
}

.piechart {
 margin: 0 auto;
 max-width: fit-content;
}
</style>
