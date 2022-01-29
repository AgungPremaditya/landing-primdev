<script lang="ts" setup>
import 'boxicons/css/boxicons.min.css'
</script>
<template>
  <div>
    <footer>
      <div class="footer-text">
        <span>Made With ❤️ From Leader & Co.</span>
      </div>
      <div class="brand">
        <img src="~/assets/images/logo.png" alt="logo" height="70" />
        <h1>Primakara <span>Developer</span></h1>
      </div>
      <div class="social-media">
        <NuxtLink to="#">
          <i class='bx bxl-github'></i>
        </NuxtLink>
        <NuxtLink to="#">
          <i class='bx bxl-facebook-square'></i>
        </NuxtLink>
        <NuxtLink to="#">
          <i class='bx bxl-instagram'></i>
        </NuxtLink>
      </div>
    </footer>
  </div>
</template>
<style scoped lang="scss">
@import url("~/assets/styles/main.css");
$footer-font: 25px;
footer{
  align-items: center;
  bottom: 0;
  display: flex;
  justify-content: space-between;
  padding: 8px 100px;
  position: relative;
  .footer-text{
    display: flex;
    justify-content: center;
    width: 30%;
  }
  .brand {
    align-items: center;
    display: flex;
    justify-content: center;
    width: 40%;
    h1 {
      color: rgb(80, 78, 78); // ! this is just a temporary color
      font-size: $footer-font;
      font-weight: 100;

      span {
        font-weight: 700;
      }
    }
  }
  .social-media{
    display: flex;
    font-size: $footer-font;
    justify-content: center;
    width: 30%;
    i.bx{
      color: rgb(80, 78, 78);
      margin: 0 15px 0 15px;
    }
  }
}

</style>
