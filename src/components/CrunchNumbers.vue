<template>
<div class="column">
                  <div class="columnchart">
                    <p><strong>Daily Progress</strong><br>Working Hours</p>
                    <div class="timeline_selector">
                      <select class="timeline" id="timeline" name="timeline_selector">
                        <option selected value="week">this week</option>
                        <option value="month">this month</option>
                        <option value="year">this year</option>
                      </select>
                    </div>
                   <div class="linecolumn_chart-wrapper">
                <apexchart type="line" height="330" width="590" :options="chartOptions" :series="series"></apexchart>
               </div>
</div>
</div>
</template>

<script>
export default {
       data: function() {
      return {
        chartOptions: {
    chart: {
    type: 'line',
    toolbar: {
      show: false,
              },
          },
          
   dataLabels: {
    enabled: false,
    enabledOnSeries: [1]
  },

legend: {
  show: false,
},
   markers: {
    size: 5,
    colors: ['#FFC400'],
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
    }
},
  colors: ['#A489D3', '#FFC400'],
  fill: {
    type: 'gradient',
    gradient: {
      shade: 'dark',
      type: "vertical",
      shadeIntensity: 1,
      gradientToColors: ['#7b56bd'], // optional, if not defined - uses the shades of same color in series
      inverseColors: false,
      opacityFrom: 1,
      opacityTo: 1,
      stops: [20, 70, 100],
      colorStops: []
    }
  },

    stroke: {
    width: [0, 2]
  },

          xaxis: {
            type: 'datetime',
  format: 'dd/MM',
   labels: {
      datetimeFormatter: {
        year: 'YYYY',
        month: 'MM',
        day: 'dd.MM',
        hour: 'HH:mm',
      }
    },

            categories: ["2021-05-30", "2021-05-31", "2021-06-01", "2021-06-02", "2021-06-03", "2021-06-04", "2021-06-05"]
          }
        },
       series: [{
    type: 'column',
    data: [50, 30, 60, 50, 60, 65, 68],
  }, {
    name: 'Social Media',
    type: 'line',
    data: [50, 30, 60, 50, 60, 65, 68]
  }],
      }
    },
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.column {
   font-family: 'Avenir Next Cyr', sans-serif;
  float: left;
  width: 800px;
  display: flex;
  position: absolute;
    margin-left: 630px;
    top: 894px;

}

.title .timeline_selector {
  display: flex;
  float: right;
  width: 100px;
  font-size: 14px;
  color: #78909c;
  align-items: center;
  margin-right: 45px;
}

.title .timeline_selector select {
  background-color: #cfd8dc;
}

.timeline_selector select {
  margin-left: 5px;
  padding: 5px;
  background-color: #cfd8dc;
  width: 100px;
  height: 40px;
  border-radius: 45px;
  border: none;
  color: #37474f;
}

.timeline_selector option {
  padding: 15px;
}

.timeline_selector select:focus {
  outline: none;
  border: none;
}

.columnchart p {
  padding: 20px 0 0 20px;
  font-size: 13px;
  color: #78909c;
  line-height: 20px;
}

.columnchart strong {
  color: #37474f;
  font-weight: normal;
  font-size: 21px;
}

.columnchart {
height: 480px;
background-color: #ffffff;
width: 620px;
}


.columnchart select {
  float: right;
  margin: -40px 40px 0 0;
  background-color: #ffffff;
  width: 130px;
  height: 30px;
  border: none;
  color: #5f6c72;
  text-transform: uppercase;
  font-size: 14px;
}

.columnchart option {
  color: #5f6c72;
  padding: 15px;
}

.linecolumn_chart-wrapper { 
     display: flex;
     float: left;
     align-items: left; 
     justify-content: left;
}

</style>