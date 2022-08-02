<template>
 <div>
    <ul id="main-nav">
      <li v-for="item in items" :key="item.title">
          {{ item.title }}
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  el: '#main-nav',
  data: function() {
      return {
    items: [
      { title: 'Home' },
      { title: 'Time Managment' },
      { title: 'Inbox' },
      { title: 'Calendar' },
      { title: 'Analytics' },
      { title: 'Settings' }
    ],
      }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#main-nav {
  margin: 0;
  padding: 0;
  float: left;
  width: 230px;
  min-height: 400vh;
  list-style: none;
  background-color: #37474f;
}

#main-nav li {
  display: flex;
  vertical-align: middle;
  justify-content: left;
  background-color: #37474f;
  opacity: 0.5;
  padding: 20px 0 20px 55px;
}

#main-nav li:first-child {
  background: url("icons/nav_home.png") 10% 50% no-repeat
}

#main-nav li:nth-child(2) {
   background: url("icons/nav_clocks.png") 10% 50% no-repeat;
}

#main-nav li:nth-child(3) {
   background: url("icons/nav_inbox.png") 10% 50% no-repeat;
}

#main-nav li:nth-child(4) {
   background: url("icons/nav_calendar.png") 10% 50% no-repeat;
}

#main-nav li:nth-child(5) {
   background: url("icons/nav_activity.png") 10% 50% no-repeat;
}

#main-nav li:last-child {
   background: url("icons/nav_settings.png") 10% 50% no-repeat;
}

#main-nav li:hover {
  background-color: #455a64;
  opacity: 1;
  cursor: pointer;
}

#main-nav li:active {
  background-color: #df468e;
}

#main-nav {
  vertical-align: middle;
  text-decoration: none;
  font-size: 14px;
  font-style: normal;
  text-align: left;
  color: #ffffff;
  width: 230px;
}

#main-nav a:hover {
  width: 230px;
  color: #ffffff;
}

#main-nav a:active {
  width: 230px;
  color: #ffffff;
}

#main-nav .image {
    position: absolute;
    padding-left: 40px;
    left: -10px;
    height: 16px;
    width: 16px;
}
</style>
