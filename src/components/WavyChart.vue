<template>
 <div class="wavylines">
              <div class="timeline_selector">
                <label for="timeline"></label>
                <select class="timeline" id="timeline" name="timeline_selector">
                  <option v-for="option in options" :key="option.title">
                  {{ option.title }}
                  </option>
                </select>
              </div>
                <p><strong>Wavy Lines</strong><br>Working Hours</p>
              <div class="chart-wrapper">
                <apexchart width="950" height="300" type="area" :options="chartOptions" :series="series"></apexchart>
               </div>
              </div>
</template>

<script>
export default {
       data: function() {
      return {
    options: [
      { title: 'This Week' }, 
      { title: 'This Month'},
      { title: 'This Year'}
    ],
        chartOptions: {
          chart: {
            id: 'vuechart-example', 
            toolbar: {
              show: false,
              },
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.timeline_selector {
  display: flex;
  float: right;
  width: 120px;
  padding-top: 35px;
  font-size: 14px;
  color: #78909c;
  position: relative;
  align-items: center;
  margin-right: 40px;
}

.timeline_selector select {
  background-color: #ffffff;
}

.timeline_selector select {
  margin-left: 5px;
  padding: 5px;
  background-color: #ffffff;
  width: 120px;
  height: 40px;
  border-radius: 45px;
  border: none;
  color: #37474f;
  text-transform: uppercase;
}

.timeline_selector option {
  padding: 15px;
  text-transform: uppercase;
}

.timeline_selector select:focus {
  outline: none;
  border: none;
}

.wavylines {
  font-family: 'Avenir Next Cyr', sans-serif;
  width: 950px;
  margin-left: 300px;
  height: 465px;
  background-color: #ffffff;
}

.wavylines p {
  max-width: 800px;
  text-align: left;
  justify-content: left;
  padding: 35px 0 30px 20px;
  font-size: 13px;
  color: #78909c;
  line-height: 20px;
}

.wavylines strong {
  color: #37474f;
  font-weight: normal;
  font-size: 21px;
}

.chart-wrapper { 
     display: flex; 
     align-items: left; 
     justify-content: left;
}
</style>