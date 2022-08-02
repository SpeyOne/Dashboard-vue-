<template>
  <div id="app">
    <PageHeader/>
    <NavBarVF/>
    <DashBoard/>
    <WavyChart/>
    <CrunchBoard/>
    <ThreeRowChart/>
    <CrunchNumbers/>
    <ProgressBoard/>
    <ProgressBars/>
    <BottomCharts/>
    <PieChart/>
    <GeneralMenu/>
    <TotalOverdue/>
  </div>
</template>

<script>
import PageHeader from './components/PageHeader.vue'
import NavBarVF from './components/NavBarVF.vue'
import DashBoard from './components/DashBoard.vue'
import WavyChart from './components/WavyChart.vue'
import CrunchBoard from './components/CrunchBoard.vue'
import ThreeRowChart from './components/ThreeRowChart.vue'
import CrunchNumbers from './components/CrunchNumbers.vue'
import ProgressBoard from './components/ProgressBoard.vue'
import ProgressBars from './components/ProgressBars.vue'
import BottomCharts from './components/BottomCharts.vue'
import PieChart from './components/PieChart.vue'
import GeneralMenu from './components/GeneralMenu.vue'
import TotalOverdue from './components/TotalOverdue.vue'

export default {
  name: 'App',
  components: {
    PageHeader,
    NavBarVF,
    DashBoard,
    WavyChart,
    CrunchBoard,
    ThreeRowChart,
    CrunchNumbers,
    ProgressBoard,
    ProgressBars,
    BottomCharts,
    PieChart,
    GeneralMenu,
    TotalOverdue
  }
}
</script>

<style>
#app {
  min-width: 1040px;
  margin: 0;
  padding: 0;
  min-height: 410vh;
  font-family: "Myriad Pro", 'Myriad', "Liberation Sans", "Nimbus Sans L", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 16px;
  line-height: 24px;
  color: #404040;
  background-color: #f5f5f5;
}
</style>
