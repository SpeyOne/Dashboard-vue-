<template>
  <div class="page-header">
    <div class="header-logo">
      <a href="#">@just<b>Free</b></a>
    </div>
    <div class="search-box">
      <input type="text" class="search-bar" placeholder="Search" />
    </div>
    <div class="profile-box">
      <a href="#" class="notifications"></a>
      <div class="nots_counter"></div>
      <div class="username">
        <select class="user-select" id="username" name="username_selector">
          <option value="first">Filip J.</option>
        </select>
        <a href="#" class="avatar"><p>F</p></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PageHeader",
};
</script>

<style scoped>
.page-header {
 display: flex;
 flex-direction: row;
 width: 100%;
 height: 70px;
 background-color: #e0e0e0;
}

.header-logo {
 display: flex;
 min-width: 230px;
 height: 70px;
 background-color: #1e88e5;
}

.header-logo a {
 margin: 20px 0 0 65px;
 color: #ffffff;
 font-weight: normal;
 font-size: 18px;
 text-decoration: none;
}

.search-box {
 display: flex;
 height: 70px;
 width: 100%;
 background: url(icons/search.png) no-repeat 34px 50%;
}

.search-box .search-bar {
 width: 300px;
 text-align: left;
 align-self: center;
 margin-left: 65px;
 padding: 15px;
 padding-left: 5px;
 color: #7e8e9f;
 font-size: 16px;
 appearance: none;
 border: none;
 outline: none;
 background-color: #e0e0e0;
 transition: 0.4s;
}

.search-bar::placeholder {
 color: #7e8e9f;
}

.search-box .search-bar:focus {
 background-color: rgba(255, 255, 255, 0.25);
 box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.05);
 border-radius: 10px;
}

.profile-box {
 display: flex;
 flex-direction: row;
 justify-content: right;
 width: 200px;
 padding-right: 32px;
 background-color: #e0e0e0;
}

.profile-box .notifications {
 padding: 0 0 0 10px;
 width: 45px;
 height: 25px;
 border-right: 2px solid #c0c8d1;
 margin-top: 22px;
 background: url(icons/not_bell.png) no-repeat 10% 50%;
}

.nots_counter {
 position: absolute;
 width: 15px;
 height: 15px;
 border-radius: 50%;
 color: #ffffff;
 background-color: #1e88e5;
 margin: 20px 150px 0 0;
 z-index: 1000;
}

.nots_counter::after {
 position: absolute;
 top: -4px;
 left: 5px;
 font-size: 10px;
 content: "8";
}

.profile-box .username {
 display: flex;
 flex-wrap: nowrap;
}

.user-select {
 margin-left: 15px;
 background-color: #e0e0e0;
 border: none;
 outline: none;
 color: #37474f;
}

.user-select select {
 background-color: #e0e0e0;
}

.avatar {
 color: #ffffff;
 background-color: #37474f;
 height: 40px;
 width: 40px;
 border-radius: 50%;
 margin: 13px 0 0 5px;
 text-decoration: none;
}

.avatar p {
 font-size: 18px;
 font-weight: bold;
 margin: 8px 0 0 14px;
}
</style>
