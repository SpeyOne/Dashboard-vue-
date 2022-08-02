<template>
<div class="progress_board">
   <div class="title">
                <p><strong>Current Progress</strong><br>This table will show you how your current projects are behaving.</p>
              </div>
              <div class="current_projects">
                <div class="projects-list">
                </div>
              </div>
</div>
</template>

<script>
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

.progress_board {
  font-family: 'Avenir Next Cyr', sans-serif;
  margin-left: 300px;
  width: 950px;
}

.projects-list {
  width: 100%;
 }

.title {
  margin: 50px 0 40px 0;
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

</style>