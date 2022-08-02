<template>
<div class="threerowchart">
    <div class="first_row">
        <p><strong>96</strong><br>Working Hours</p>
        <div class="columns">
            <div class="first_column"></div>
            <div class="second_column"></div>
            <div class="third_column"></div>
            </div>
            </div>
            <div class="second_row">
                <p><strong>1,204</strong><br>Converstaions</p>
                <div id="linechart_wrapper">
        <apexchart type="line" width="170" height="110" :options="chartOptions" :series="series"></apexchart>
      </div>
                </div>
                <div class="third_row">
                    <p><strong>7</strong><br>People</p>
                    <div class="circles">
                        <div class="first_circle"></div>
                        <div class="second_circle"></div>
                        <div class="third_circle"></div>
                        <div class="fourth_circle"></div>
                        <div class="fifth_circle"></div>
                        <div class="sixth_circle"></div>
                        <div class="seventh_circle"></div>
                        </div>
                        </div>
                    </div>
</template>

<script>
export default {
       data: function() {
      return {
                series: [{
              name: "Desktops",
              data: [800, 700, 850, 800, 900, 1000, 1204, 1100, 1000, 900]
          }],
          chartOptions: {
            chart: {
              height: 350,
              type: 'line',
              toolbar: {
                  show: false,
              },
              zoom: {
                enabled: false
              }
            },
            dataLabels: {
              enabled: false
            },
            stroke: {
              curve: 'smooth',
              colors: ['#ec407a']  
            },
            grid: {
                show: false,
              row: {
                opacity: 0,
              },
            },
              xaxis: {
    labels: {
        show: false,
        showDuplicates: false,
        trim: false,
    },
    axisBorder: {
        show: false,
    },
    axisTicks: {
        show: false,
    },
    crosshairs: {
        show: false,
        },
    },
     yaxis: {
        show: false,
        showAlways: false,
        showForNullSeries: false,
        seriesName: undefined,
        opposite: false,
        reversed: false,
        logarithmic: false,
        forceNiceScale: false,
        floating: false,
        decimalsInFloat: undefined,
        labels: {
            show: false,
        },
        axisBorder: {
            show: false,
        },
        axisTicks: {
            show: false,
        },
        crosshairs: {
            show: false,
        },
        tooltip: {
            enabled: false,
            offsetX: 0,
        },
        
    }
          }}}};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

.threerowchart {
  display: flex;
  flex-direction: column;
  text-align: center;
  flex-wrap: wrap;
  width: 315px;
  height: 480px;
  background-color: #ffffff;
  vertical-align: middle;
  margin: 0 17px 10px 300px;
  font-family: 'Avenir Next Cyr', sans-serif;
}

.first_row,
.second_row,
.third_row {
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  margin: 10px 0;
  max-height: 170px;
}

.first_row,
.second_row {
  border-bottom: 2px solid #ebedef;
}

.third_row {
    padding: 0;
    margin: 0;
}

.threerowchart p {
  color: #cfd8dc;
  padding: 30px 0 40px 0;
  margin-left: 35px;
  font-size: 13px;
}

.threerowchart strong {
  font-size: 21px;
  color: #37474f;
  font-weight: normal;
}

.first_row .columns {
  display: inline;
  width: 130px;
  height: 104px;
  display: flex;
  margin: 0 0 22px 40px;
}

.first_column {
  width: 30px;
  height: 104px;
  margin-right: 20px;
  background-image: linear-gradient(to bottom, #a5cff5 25%, #61abed 25%, #61abed 50%, #1e88e5 50%, #1e88e5 20%);
}

.second_column {
  width: 30px;
  height: 104px;
  margin-right: 20px;
  background-image: linear-gradient(to bottom, #a5f6e2 33%, #60f0cc 25%, #60f0cc 65%, #1de9b6 50%, #1de9b6 25%);
}

.third_column {
  width: 30px;
  height: 104px;
  background-image: linear-gradient(to bottom, #cbbce7 25%, #a489d4 25%, #a489d4 50%, #7e57c2 50%, #7e57c2 20%);
}

.first_column:hover,
.second_column:hover,
.third_column:hover {
  filter:hue-rotate(45deg);
}

.second_row {
  height: 100px;
  margin-top: 50px;
}

.third_row {
 padding-top: 25px;
  height: 100px;
}

.third_row p {
  padding: 0;
  margin: 0 0 30px 55px;
}

.threerowchart .circles {
  display: flex;
  margin: 0 0px 15px 60px;
  flex-wrap: wrap;
  width: 160px;
  height: 75px;
}

.circles div {
  background-color: #b0bec5;
  height: 32px;
  width: 32px;
  border-radius: 50%;
  margin-right: 8px;
}

.circles div:nth-child(2n) {
  background-color: #cfd8dc;
}

.circles div:hover {
  filter: brightness(75%);
}


</style>