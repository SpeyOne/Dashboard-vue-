<template>
          <div class="total_overdue">
              <div class="overdue_chart">
                  <p><strong>Total Overdue</strong><br>I need Dollars</p>
                  <b>$14,220</b>
                   <div class="chart">
        <apexchart type="line" width="285" height="200" :options="chartOptions" :series="series"></apexchart>
      </div>
                </div>
            </div>
</template>

<script>
export default {
         data: function() {
      return {
          series: [{
              name: "Total",
              data: [8, 12, 21, 22, 26, 25, 20]
          }],

        chartOptions: {
            colors: ['#9a7dcf'],
xaxis: {
  categories: ['S', 'M', 'T', 'W', 'T', 'F', 'S'],
},
          chart: {
            id: 'vuechart-example', 
            zoom: {
    enabled: false
  }
          },
          
  dataLabels: {
    enabled: false,
  },
  stroke: {
  curve: 'straight'
},

    markers: {
    size: 5,
    colors: ['#9374cc'],
    strokeOpacity: 1,
    strokeDashArray: 0,
    fillOpacity: 1,
    discrete: [],
    shape: "circle",
    radius: 0,
    offsetX: 0,
    offsetY: 0,
    onClick: undefined,
    onDblClick: undefined,
    showNullDataPoints: true,
    hover: {
      size: undefined,
      sizeOffset: 3
    },
        }}}}};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

.total_overdue {
 font-family: 'Avenir Next Cyr', sans-serif;
 width: 305px;
 height: 500px;
 background-color: #ffffff;
 margin-left: 945px;
 border: 1px solid #f2f3f3;
 text-align: center;
 margin-top: -502px;
}

.overdue_chart p {
  margin: 20px 0 0 15px;
  font-size: 13px;
  color: #78909c;
  line-height: 20px;
  text-align: left;
}

.overdue_chart strong {
  font-size: 21px;
  color: #37474f;
  font-weight: normal;
}

.overdue_chart b {
  position: relative;
  font-size: 32px;
  color: #37474f;
  font-weight: normal;
  top: 65px;
  margin-bottom: 65px;
}

.chart {
    margin-top: 100px;
    }

</style>