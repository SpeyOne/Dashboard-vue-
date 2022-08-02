<template>
<div class="crunch_numbers">
  <div class="title">
                <p><strong>Crunch some Numbers</strong><br>See how your projects are progressing via the new statistics engine.</p>
                <div class="timeline_selector">
                  <label>Timeline:</label>
                  <select class="timeline" id="timeline" name="timeline_selector">
                    <option value="first">3 Days</option>
                    <option selected value="second">7 Days</option>
                    <option value="third">Month</option>
                  </select>
                </div>
                </div>
                <div class="crunch_board">
                <div class="crunch_charts">
                </div>
              </div>
</div>
</template>

<script>
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.crunch_numbers {
  font-family: 'Avenir Next Cyr', sans-serif;
  margin-left: 300px;
  width: 950px;
}

.title {
  margin: 50px 0 40px 0;
  text-align: left;
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

.crunch_charts {
 width: 950px;
  display: flex;
  justify-content: space-between;
}

</style>