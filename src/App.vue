<template>
  <div class="custom-container">
    <div class="bg-img-container">
      <img class="bg-img" src="./assets/background-pattern-desktop.svg" alt="">
    </div>
    <div class="card-container">
      <CardComponent/>
    </div>
  </div>
</template>

<script setup>
import CardComponent from "./components/CardComponent.vue";

</script>

<style>
*{
  margin:0px;
  padding:0px;
  box-sizing: border-box;
  font-family: 'Roboto', sans-serif;
}

body{
  background: #F9EEFF;
}

.custom-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}

.bg-img-container{
  position: absolute;
  top:0;
  z-index: -1;
  width:100%;
}

.bg-img{
  width:100%;
}

@media only screen and (max-width: 767px) {
  .bg-img-container{
    height: 400px;
    overflow: hidden;
  }
  .bg-img{
    width:auto;
  }
}

</style>