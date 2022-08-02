<template>
 <div>
    <link href="http://fonts.cdnfonts.com/css/avenir-next-cyr" rel="stylesheet">
    <div class="dashboard">
     <div class="title">
        <p><strong>Hi Filip,</strong><br>Checkout your latesr projects and their progress.</p>
     </div>
    </div>
 </div>
</template>

<script>
export default {
  name: 'DashBoard',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

.dashboard {
  margin: 0 80px 40px 300px;
  font-family: 'Avenir Next Cyr', sans-serif;
}

.title {
  margin: 50px 0 50px 0;
  text-align: left;
  padding-bottom: 25px;
  border-bottom: 2px solid #dee3e7;
}

.title p {
  color: #78909c;
  font-size: 14px;
  line-height: 21px;
}

.title strong {
  color: #37474f;
  font-size: 20px;
  font-weight: normal;
}

.title .timeline_selector {
  display: flex;
  float: right;
  width: 100px;
  font-size: 14px;
  color: #78909c;
  position: relative;
  top: -40px;
  align-items: center;
  margin-right: 40px;
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
</style>
