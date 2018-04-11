<template>
    <div class="imgLogo">
        <img class="logo" src="/src/assets/2000px-Vue.svg.png">
        <div class="shadowBox"></div>
    </div>
</template>
<script>
export default {};
</script>
<style>
.imgLogo {
  position: relative;
  margin-left: 41%;
  overflow: visible;
  z-index: 1;
  & .logo {
    position: absolute;
    bottom: -601px;
    margin-left: 24px;
    z-index: 1;
    width: 997px;
  }
  & .shadowBox {
    position: absolute;
    top: -204px;
    left: -560px;
    height: 2125px;
    width: 867px;
    -webkit-transform: rotate(30deg);
    transform: rotate(30deg);
    background-color: #35495e;
    z-index: -1;
  }
}
</style>
