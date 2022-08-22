<template>
  <div class="general_menu">
    <div class="profile_photo">
      <div class="online_status"></div>
    </div>
    <p><strong>Jake Applessed</strong><br />London, UK</p>
    <table class="profile-table">
      <tr>
        <td>Working hours<br /><strong>14 hours</strong></td>
        <td>Ammount Total<br /><strong>$ 6,269</strong></td>
      </tr>
      <tr>
        <td>Overdue<br /><strong>$ 829</strong></td>
        <td>% overall work<br /><strong>48%</strong></td>
      </tr>
    </table>
    <a href="#">Send Invoice</a>
  </div>
</template>

<script></script>

<style>
.general_menu {
 font-family: "Avenir Next Cyr", sans-serif;
 width: 310px;
 height: 500px;
 background-color: #ffffff;
 margin-right: 10px;
 margin-left: 625px;
 border: 1px solid #f2f3f3;
 text-align: center;
 margin-top: -502px;
}

.profile_photo {
 margin: 35px auto 30px auto;
 width: 100px;
 height: 100px;
 border-radius: 50%;
 background: url(profilephoto.jpg) no-repeat 50% 50%;
 background-size: 200%;
}

.online_status {
 position: relative;
 background-color: #4bcf99;
 width: 16px;
 height: 16px;
 top: 80px;
 left: 75px;
 border-radius: 50%;
 border: 4px solid #ffffff;
}

.profile-table {
 width: 332px;
 margin-bottom: 40px;
 border-collapse: collapse;
 text-align: left;
 color: #000000;
}

.profile-table td {
 border: 1px solid #f2f4f7;
 padding: 15px 10px 15px 25px;
 font-size: 14px;
 color: #a1b1c2;
 text-align: left;
}

.profile-table td strong {
 font-size: 21px;
 color: #37474f;
 font-weight: normal;
}

.general_menu a {
 color: #df468e;
 font-size: 14px;
 font-weight: bolder;
 margin-bottom: 40px;
}
</style>
