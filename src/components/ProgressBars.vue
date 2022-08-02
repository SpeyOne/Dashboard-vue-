<template>
<div class="progress_board">
  <div class="project">
                    <div class="project_preview"></div>
                    <p class="title"><strong>Project Title</strong><br>Design & Development</p>
                    <p class="update_time">Last updated Today at 4:24 AM</p>
                    <p class="clocks">26:30</p>
                    <p class="project_comments">624</p>
                    <div class="project_progress load_15"><span style="width: 0%"></span></div>
                  </div>
                  <div class="project">
                    <div class="project_preview"></div>
                    <p class="title"><strong>Project Title</strong><br>Design & Development</p>
                    <p class="update_time">Last updated Today at 4:24 AM</p>
                    <p class="clocks">26:30</p>
                    <p class="project_comments">624</p>
                    <div class="project_progress load_90"><span style="width: 0%"></span></div>
                  </div>
                  <div class="project">
                    <div class="project_preview"></div>
                    <p class="title"><strong>Project Title</strong><br>Design & Development</p>
                    <p class="update_time">Last updated Today at 4:24 AM</p>
                    <p class="clocks">26:30</p>
                    <p class="project_comments">624</p>
                    <div class="project_progress load_85"><span style="width: 0%"></span></div>
                  </div>
                  <div class="project">
                    <div class="project_preview"></div>
                    <p class="title"><strong>Project Title</strong><br>Design & Development</p>
                    <p class="update_time">Last updated Today at 4:24 AM</p>
                    <p class="clocks">26:30</p>
                    <p class="project_comments">624</p>
                    <div class="project_progress load_30"><span style="width: 0%"></span></div>
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
  margin-bottom: 45px;
}

.project {
  display: flex;
  flex-direction: row;
  width: 100%;
  height: 105px;
  background-color: #ffffff;
  margin-bottom: 10px;
  align-items: center;
  justify-content: space-evenly;
 }

 .project p {
  height: 25px;
  font-size: 13px;
  color: #37474f;
}

 .project_preview {
  width: 60px;
  height: 60px;
  border-radius: 2px;
  background-color: #cfd8dc;
 }

 .project .title {
  font-size: 14px;
  color: #78909c;
  border: none;
  line-height: 21px;
  margin-top: 25px;
  margin-right: 50px;
 }

 .project .title strong {
  font-size: 18px;
  color: #37474f;
 }

 .project .update_time {
  border-right: 2px solid #dbe1e8;
  padding-right: 30px;
 }

 .project .clocks {
  background: url(icons/clocks.png) no-repeat left;
  padding-left: 30px;
}

.project .project_comments {
  float: right;
  background: url(icons/comments.png) no-repeat left;
  padding-left: 30px;
}

@keyframes load15 { 
  100% { 
    padding-left: 15%; 
  }
}

@keyframes load90 { 
  100% { 
    padding-left: 90%; 
  }
}

@keyframes load85 { 
  100% { 
    padding-left: 85%; 
  }
}

@keyframes load30 { 
  100% { 
    padding-left: 30%; 
  }
}

.project_progress {
  width: 200px;
  height: 8px;
  position: relative;
  background-color: #cfd8dc;
  border-radius: 5px;
  margin-right: 50px;
}

.project_progress span {
  display: block;
  height: 8px;
  border-radius: 5px;
  position: relative;
  overflow: hidden;
}

.load_15 span {
  background-image: linear-gradient(to right, #e15094, #ec5b9f);
  animation-name: load15;
  animation-duration: 1.5s;
  animation-fill-mode: forwards;
}

.load_90 span {
  background-image: linear-gradient(to right, #0dc3aa, #b7fcec);
  animation-name: load90;
  animation-duration: 2s;
  animation-fill-mode: forwards;
}

.load_85 span {
  background-image: linear-gradient(to right, #327fff, #81b1ff);
  animation-name: load85;
  animation-duration: 1.5s;
  animation-fill-mode: forwards;
}

.load_30 span {
  background-image: linear-gradient(to right, #aa00ff, #ba36fc);
  animation-name: load30;
  animation-duration: 2s;
  animation-fill-mode: forwards;
}
</style>