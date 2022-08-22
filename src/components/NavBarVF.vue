<template>
  <div>
    <ul class="main-nav">
      <li>
        <a href="#" v-for="item in items" :key="item.title">
          <img width="16" height="15" alt="icon" :src="item.icon" />
          {{ item.title }}
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  el: "#main-nav",
  data: function () {
    return {
      items: [
        { icon: require("@/components/icons/nav_home.png"), title: "Home" },
        {
          icon: require("@/components/icons/nav_clocks.png"),
          title: "Time Managment",
        },
        { icon: require("@/components/icons/nav_inbox.png"), title: "Inbox" },
        {
          icon: require("@/components/icons/nav_calendar.png"),
          title: "Calendar",
        },
        {
          icon: require("@/components/icons/nav_activity.png"),
          title: "Analytics",
        },
        {
          icon: require("@/components/icons/nav_settings.png"),
          title: "Settings",
        },
      ],
    };
  },
};
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
 vertical-align: middle;
 justify-content: left;
 text-align: left;
}

.main-nav a {
 display: flex;
 opacity: 0.5;
 padding: 20px 0 20px 20px;
 text-decoration: none;
 font-size: 14px;
 font-style: normal;
 color: #ffffff;
}

.main-nav a:hover {
 background-color: #455a64;
 opacity: 1;
}

.main-nav a:active {
 background-color: #df468e;
}

.main-nav img {
 display: flex;
 padding-right: 15px;
 margin-top: 5px;
}
</style>
