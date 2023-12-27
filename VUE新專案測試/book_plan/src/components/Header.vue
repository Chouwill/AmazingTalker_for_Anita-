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
</template>





<script setup>

</script>


<style scoped>
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
</style>