<template>
    <div class="imgLogo">
        <img class="logo" src="/src/assets/2000px-Vue.svg.png">
        <div class="shadowBox"></div>
    </div>
</template>
<script>
export default {}
</script>
<style lang="postcss">
@import '../../../commons';
.imgLogo {
  position: relative;
  overflow: visible;
  z-index: 1;
  margin-left: 41%;
  & .logo {
    position: absolute;
    z-index: 1;
    margin-left: 26px;
    bottom: 370px;
    height: 185px;
        @media (--medium) {
          bottom: 521px;
          height:267px; 
        }
        @media (--medium-plus) {
          bottom: 774px;
          height:420px;
        }
        @media (--large) {
          bottom: 973px;
          height: 513px;
        }
        @media (--xlarge) {
          bottom: 816px;
          height:726px;
        }
        @media (--xlarge-plus) {
          bottom: 1596px;
          height:910px;
        }
  }
  & .shadowBox {
    position: relative;
    -webkit-transform: rotate(30deg);
    transform: rotate(30deg);
    background-color: var(--light-blue);
    z-index: -1;
    top: -82px;
    left: -96px;
    height: 469px;
    width: 183px;
      @media (--medium) {
        top: -126px;
        left: -151px;
        height: 640px;
        width: 267px;        
      }
      /* @media (width >= 768px) and (width < 830px) {
        top: -136px;
        left: -211px;
        height: 865px;
        width: 292px;
      } */
      @media (--medium-plus) {
        top: -212px;
        left: -209px;
        height: 973px;
        width: 403px;        
      }
      @media (--large) {
        top: -235px;
        left: -288px;
        height: 1225px;
        width: 500px;        
      }
      @media (--xlarge) {
        top: 98px;
        left: -406px;
        height: 1582px;
        width: 724px;       
      }
      @media (--xlarge-plus) {
        top: -306px;
        left: -562px;
        height: 2125px;
        width: 910px;
        
      }
  }

}
</style>
