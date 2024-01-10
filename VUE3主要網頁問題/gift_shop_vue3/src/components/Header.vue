<template>
  <header>
    <div class="search_box">
      <input type="search" value="Search" />
    </div>
    <nav>
      <div class="nav_logo">
        <a href="#"><h1>JSY</h1></a>
      </div>
      <div class="menu">
        <a href="#">HOME & LiVING</a>
        <a href="#">Accessories</a>
        <a href="#">Stationery</a>
        <a href="#">Sale</a>
        <a href="#">Gift Card</a>
      </div>
    </nav>
    <ul class="user">
      <li>
        <a href="#"><i class="fa-solid fa-user"></i></a>
        <h4>Log In</h4>
      </li>
      <li>
        <h4>Cart (0)</h4>
      </li>
    </ul>
    <!-- <img src="https://static.wixstatic.com/media/c837a6_327e6bf04c1c4443ad6c4f13728c41fb~mv2.jpg/v1/fill/w_1903,h_511,al_r,q_85,usm_0.66_1.00_0.01,enc_auto/c837a6_327e6bf04c1c4443ad6c4f13728c41fb~mv2.jpg" alt=""> -->
  </header>
</template>

<script setup></script>

<style scoped>
header {
  display: grid;

  width: 100%;
  grid-template-columns: repeat(5, 240px);
  grid-template-rows: repeat(3, 50px);
  grid-gap: 10px;
  background-color: yellowgreen;
  box-sizing: border-box;
}
.search_box {
  line-height: 3;
  background-color: aqua;
  grid-row-start: 2;
  grid-row-end: 3;
}
nav {
  width: 550px;
  text-align: center;
  background-color: orangered;
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 2;
  grid-row-end: 3;
  margin-left: 50px;
}
.nav_logo {
  line-height: 2;
}
.menu {
  width: 100%;
  margin: 15px 0;
  background-color: burlywood;
}
.menu a {
  margin: 0 15px;
}
.user {
  width: 205px;
  background-color: palegreen;
  display: flex;
  grid-column-start: 5;
  grid-column-end: 5;
  grid-row-start: 2;
  grid-row-end: 3;
}
.user li:first-child {
  display: flex;
  justify-content: space-around;
  flex: 2;
  /* border: 2px solid red; */
}
.user li:last-child {
  flex: 1;
}
.user a,
h4 {
  font-size: 20px;
}
</style>
