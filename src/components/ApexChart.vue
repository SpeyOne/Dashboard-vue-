<template>
   <div class="chart-wrapper">
     <apexchart width="900" height="300" type="area" :options="chartOptions" :series="series"></apexchart>
   </div>
</template>

<script>
export default {
       data: function() {
      return {
        chartOptions: {
          chart: {
            id: 'vuechart-example'
          },
           toolbar: {
    show: false,
  },
  dataLabels: {
  enabled: false,
},
legend: {
  show: false,
},
           colors: ['#d7a9df', '#f9669a'],  
  fill: {
    opacity: 0.85,
    type: ['solid'],
  },
  stroke: {
  show: false,
  curve: 'smooth'
},
          xaxis: {
            categories: ["2021-05-30", "2021-05-31", "2021-06-01", "2021-06-02", "2021-06-03", "2021-06-04", "2021-06-05", "2021-06-06", "2021-06-07", "2021-06-08", "2021-06-09"]
          }
        },
        series: [{
            name: 'series1',
            data: [52, 45, 50, 45, 45, 52, 48, 50, 45, 48, 47]
          }, {
            name: 'series2',
            data: [42, 49, 43, 45, 49, 45, 48, 45, 52, 50, 48]
          }],
      }
    },
};
</script>

<style>
 div.chart-wrapper { 
     display: flex; 
     align-items: left; 
     margin-left: 300px;
     justify-content: left;
}
</style> 
