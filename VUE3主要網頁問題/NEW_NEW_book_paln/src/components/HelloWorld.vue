<script setup>
import { ref } from "vue";

defineProps({
  msg: String,
});

const count = ref(0);
</script>

<template>
  <header>
    <h1 class="logo">
      <a href="#">
        <img src="./LOGO/own_style_01.png" alt="" />
      </a>
    </h1>
    <label for="menu_control" class="menu_btn">
      <span>選單</span>
    </label>
    <nav>
      <a href="#">關於我們</a>
      <a href="#">開始Plan</a>
      <a href="#">豐富資源</a>
      <a href="#">享受放鬆生活</a>
    </nav>
  </header>
  <main>
    <div class="containter">
      <div id="calendar"></div>
      <form action="#" id="bookPlanForm">
        <ul class="left_form">
          <li>
            <label for="themeInput">主題名稱:</label>
            <input type="text" id="themeInput" />
          </li>
          <li>
            <label for="planInput">計畫名稱:</label>
            <input type="text" id="planInput" />
          </li>
          <li>
            <select id="palnKind">
              <option value="">計畫分類</option>
              <option value="進修">進修</option>
              <option value="教育">教育</option>
              <option value="休閒">休閒</option>
              <option value="工作">工作</option>
            </select>
            <p id="planKind"></p>
          </li>
          <li>
            <select id="importantKind">
              <option value="">優先度</option>
              <option value="紅">紅</option>
              <option value="綠">綠</option>
              <option value="黃">黃</option>
              <option value="橙">橙</option>
            </select>
            <p id="importantKindOutput"></p>
          </li>
        </ul>
        <ul class="right_form">
          <li>
            <label for="unitInput">單元名稱:</label>
            <input type="text" id="unitInput" />
          </li>
          <li>
            <label for="unitLocalInput">單元目標:</label>
            <input type="text" id="unitLocalInput" />
          </li>
          <li>
            <label for="startInput">開始時間:</label>
            <input type="date" id="startInput" />
          </li>
          <li>
            <label for="endInput">結束時間:</label>
            <input type="date" id="endInput" />
          </li>
        </ul>
        <div class="sent">
          <input type="button" value="提交" onclick="submitForm()" />
        </div>
      </form>
      <div id="output">
        <p id="theme"></p>
        <p id="plan"></p>
        <p id="planKind"></p>
        <p id="importantKindOutput"></p>
        <p id="start"></p>
        <p id="end"></p>
        <p id="unit"></p>
        <p id="unitLocal"></p>
      </div>
    </div>
  </main>
  <aside>
    <div class="user">
      <i class="fa-regular fa-user"></i>
      <i class="fa-solid fa-cart-shopping"></i>
    </div>
  </aside>
  <footer>
    <h1>我是Footer</h1>
  </footer>
</template>

<style scoped>
/* -------------header */
header {
  width: 100%;
  height: 50px;
  background-color: #ccc;
  position: fixed;
}
.logo {
  width: 60px;
  height: 40px;
}
.logo a{
    display: block;
    height: 40px;
}
.logo img {
  display: block;;
}
header .logo img {
  width: 60px;
  height: 40px;
}
#menu_control{
    position: absolute;
    z-index: -2;
    opacity: 0;
}
.menu_btn {
  width: 40px;
  height: 40px;
  background-color: #000;
  display: block;
  position: absolute;
  top: 5px;
  right: 10px;
}
.menu_btn span {
  opacity: 0;
  width: 1px;
  height: 1px;
  display: block;
  overflow: hidden;
}
.menu_btn::before{
    content: '';
    position: absolute;
    height: 2px;
    left: 2px;
    width: 36px;
    background-color: #aaa;
    top: 0;
    bottom: 0;
    margin: auto;
    box-shadow: 0px 8px 0px #f00,
                0px -8px 0px #aaa;
}


nav a{
    display: block;
    text-decoration: none;
    color: #a6e22c;
    padding: 10px 20px;
    border-bottom: 1px solid #a6e22c;
}
#menu_control:checked ~ header nav{
    left: 0;
}
@media screen and (max-width: 767px){
    nav{
    width: 80%;
    height: calc(100vh - 50px);/* 扣掉header 50像素 */
    background-color: #282923;
    position: absolute;
    top: 50px;
    left: -100%;
    transition: 0.5s;
    }
}
@media screen and (min-width: 768px){
    .menu_btn{
        display: none;
    }
    header{
        display: flex;
        justify-content: space-between;
        background-color: #282923;
        align-items: center;
    }
    .logo{
        margin-top: 0;
    }
    .logo a{
      display: block;
      height: 40px;
    }
    .logo img{
      display: block;
    }
    nav{
        position: relative;
        left: 0;
        display: flex;
        width: auto;
        height: auto;
        top: 0;
        background-color: transparent;
    }
    nav a{
        border-bottom: none;
    }
}
/* ---------------------main */
.containter {
    width: 100%;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }
  #calendar {
    width: 50%;
    display: flex;
    justify-content: center;
  }
  form {
    display: flex;
    justify-content: center;
    width: 1500px;
    border: 5px solid teal;
    /* flex-wrap: wrap; */
  }
  /* ------------- aside*/
  aside{
    width: 100%;
    /* background-color: chartreuse; */
    position: fixed;
    bottom: 100px;
    right: 50px;
}
.user {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center; 
    align-items: flex-end; /* 垂直居中 */
    flex-direction: column; 
   
  }
  
  .user i {
    font-size: 20px;
    z-index: 1;
    color: white;
    background-color: gray;
    border-radius: 50%;
    padding: 10px;
    margin: 20px;
  }
  /* ------------    footer*/
  footer{
    
    width: 100%;
    height: 50px;
    background-color: #e50909;
    margin-bottom: 500px;
}
footer h1{
    background-color: #e50909;
    color: #000;
}

</style>
