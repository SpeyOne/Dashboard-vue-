<template>
  <div class="progress_board">
    <div class="project" v-for="project in projects" :key="project">
      <div class="project_preview"></div>
      <p class="title" :key="project.title">{{ project.title }}</p>
      <p class="section" :key="project.section">{{ project.section }}</p>
      <p class="update_time">Last updated {{ moment().calendar() }}</p>
      <p class="clocks" :key="project.time">{{ project.time }}</p>
      <p class="project_comments" :key="project.comments">
        {{ project.comments }}
      </p>
      <div class="project_progress" :class="[project.loader]">
        <span style="width: 0%"></span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  el: "#progressbar",
  data: function () {
    return {
      projects: [
        {
          title: "Project Title",
          section: "Design & Development",
          time: "26:30",
          comments: "624",
          loader: "load_15",
        },
        {
          title: "Project Title",
          section: "Design & Development",
          time: "26:30",
          comments: "624",
          loader: "load_90",
        },
        {
          title: "Project Title",
          section: "Design & Development",
          time: "26:30",
          comments: "624",
          loader: "load_85",
        },
        {
          title: "Project Title",
          section: "Design & Development",
          time: "26:30",
          comments: "624",
          loader: "load_30",
        },
      ],
    };
  },
};
</script>

<style>
.progress_board {
 font-family: "Avenir Next Cyr", sans-serif;
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
 text-align: center;
 align-items: center;
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
 margin-left: 20px;
 margin-right: 15px;
}

.project .title {
 font-size: 18px;
 color: #37474f;
 border: none;
 line-height: 21px;
 margin-top: 30px;
}

.project .section {
 margin: 0;
 padding: 0;
 position: relative;
 margin-left: -96px;
 margin-top: 25px;
 margin-right: 70px;
 font-size: 14px;
 color: #78909c;
 float: left;
 text-align: left;
 align-items: left;
}

.project .update_time {
 border-right: 2px solid #dbe1e8;
 margin-right: 20px;
 padding-right: 30px;
}

.project .clocks {
 background: url(icons/clocks.png) no-repeat left;
 padding-left: 30px;
 margin-right: 20px;
}

.project .project_comments {
 float: right;
 background: url(icons/comments.png) no-repeat left;
 padding-left: 30px;
 margin-right: 20px;
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
 width: 190px;
 height: 8px;
 position: relative;
 background-color: #cfd8dc;
 border-radius: 5px;
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
