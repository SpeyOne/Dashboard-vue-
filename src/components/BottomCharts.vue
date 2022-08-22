<template>
  <div class="bottom_charts">
    <div class="title">
      <p>
        <strong>Crunch some Numbers</strong><br />See how your projects are
        progressing via the new statistics engine.
      </p>
      <div class="timeline_selector">
        <label>Timeline:</label>
        <select class="timeline" id="timeline" name="timeline_selector">
          <option v-for="option in options" :key="option.title">
            {{ option.title }}
          </option>
        </select>
      </div>
    </div>
    <div class="profile_stats"></div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      options: [{ title: "3 Days" }, { title: "7 Days" }, { title: "Month" }],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.bottom_charts {
 font-family: "Avenir Next Cyr", sans-serif;
 margin-left: 300px;
 width: 950px;
 background-color: #f5f5f5;
 margin-bottom: 25px;
}

.profile_stats {
 display: flex;
 flex-direction: row;
}

.title {
 margin: 50px 0 20px 0;
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
</style>
