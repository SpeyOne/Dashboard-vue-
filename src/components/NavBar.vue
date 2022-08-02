<template>
 <div>
    <ul class="main-nav">
      <li><a href="#"><img src="..//components/nav_home.png" width="16" height="15"/>Home</a>
      </li>
      <li><a href="#"><img src="..//components/nav_clocks.png" width="16" height="16"/>Time Managment</a>
      </li>
      <li><a href="#"><img src="..//components/nav_inbox.png" width="16" height="14"/>Inbox</a>
      </li>
      <li><a href="#"><img src="..//components/nav_calendar.png" width="16" height="16"/>Calendar</a>
      </li>
      <li><a href="#"><img src="..//components/nav_activity.png" width="16" height="10"/>Analytics</a>
      </li>
      <li><a href="#"><img src="..//components/nav_settings.png" width="16" height="16"/>Settings</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.main-nav {
  margin: 0;
  padding: 0;
  float: left;
  width: 230px;
  min-height: 400vh;
  list-style: none;
  background-color: #37474f;
}

.main-nav li {
  display: flex;
  vertical-align: middle;
  justify-content: left;
  background-color: #37474f;
  opacity: 0.5;
}

.main-nav li:hover {
  background-color: #455a64;
  opacity: 1;
}

.main-nav li:active {
  background-color: #df468e;
}

.main-nav a {
  padding: 20px 0 20px 0;
  vertical-align: middle;
  text-decoration: none;
  font-size: 14px;
  font-style: normal;
  text-align: left;
  padding-left: 21px;
  color: #ffffff;
  width: 230px;
}

.main-nav a img {
  margin-right: 15px;
  vertical-align: middle;
}

.main-nav a:hover {
  width: 230px;
  color: #ffffff;
}

.main-nav a:active {
  width: 230px;
  color: #ffffff;
}
</style>
