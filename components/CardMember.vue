<script lang="ts" setup>

</script>
<template>
  <div>
    <div class="card">
      <div class="card-body">
        <div class="card-img">
          <img src="~/assets/images/favicon.png">
        </div>
        <div class="card-text">
          <p>ADI</p>
          <span>The Founder</span>
        </div>
      </div>
    </div>  
  </div>
</template>
<style scoped lang="scss">
@import url("~/assets/styles/main.css");
.card{
  align-items: center;
  // background-color: #777;
  display: flex;
  height: 150px;
  justify-content: center;
  margin: 2rem;
  max-width: 16.66%;
  .card-body{
    align-items: center;
    background-color: #272727;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    height: 100%;
    justify-content: center;
    padding: 16px;
    width: 100%;
    .card-img{
      background-color: #fff;
      border-radius: 100%;
      margin-bottom: 20px;
      max-height: 50px;
      max-width: 50px;
      img{
        height: 100%;
        width: 100%;
      }
    }
    .card-text{
      text-align: center;
        color: #fff;
      p{
        font-size: 16px;
        line-height: 1.5;
      }
      span{
        font-size: 12px;
      }
    }
  }
}

</style>