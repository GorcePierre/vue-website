<template>
    <div class="bodyBlock">
        <section class="firstBackEffect"></section>
        <section class="secondBackEffect"></section>
        <section class="thirdBackEffect">
            <article class="subThirdEffect"></article>
        </section></div>
</template>
<script>
export default { }
</script>
<style lang="postcss">
@import '../../../commons';

.bodyBlock {

  position: relative;
  overflow: hidden;
  background-color: var(--light-blue);
  height: 1797px;
  width: 100%;
  z-index: -3;
  margin-top: -16%;
      @media  (width >= 681px) and (width <= 831px) {
        margin-top: -13%;
      }

  & .firstBackEffect {
    position: relative;
    background-color: var(--dark-blue);
    z-index: 0;
    opacity: 0.6;
    height: 226px;
    width: 155px;
      @media (--medium) {
        height: 317px;
        width: 155px;
      }
      @media (--medium-plus) {
        height: 410px;
        width: 170px;
      }
      @media (--large) {
        height: 625px;
        width:240px; 
      }
      @media (--xlarge) {
        height: 770px;
        width:294px; 
      }
      @media (--xlarge-plus) {
        height: 846px;
        width:375px; 
        
      }
  }

  & .secondBackEffect {
    position: relative;
    background-color: var(--dark-blue);
    -webkit-transform: rotate(30deg);
    transform: rotate(30deg);
    z-index: 0;
    opacity: 0.6;
    height: 1630px;
    width: 168px;
    left: 382px;
    top: 88px;
      /* @media (width >= 768px) and (width <= 831px){
        height: 2010px;
        width: 363px;
        left: 412px;
      } */
      @media (--medium-plus) {
        height: 2050px;
        width: 362px;
        left: 489px;
      }
      @media (--large) {
        height: 3258px;
        width: 276px;
        left: 601px;
        top:-819px
      }
      @media (--xlarge) {
        height: 4958px;
        width: 276px;
        left: 648px;
        top:-864px        
      }
  }

  & .thirdBackEffect {
    position: relative;
    background-color: var(--dark-blue);
    transform: rotate(30deg);
    z-index: 0;

      @media (--medium) {
        
      }
      @media (--medium-plus) {
        
      }
      @media (--large) {
        
      }
      @media (--xlarge) {
        
      }
      @media (--xlarge-plus) {
        top: -52.5%;
        height: 33%;
        width: 16%;
        right: -29.2%;
        
      }
    }
    & .subThirdEffect {
      position: absolute;
      background-color: var(--light-blue);
      -webkit-transform: rotate(60deg);
      transform: rotate(60deg);

      @media (--medium) {
        
      }
      @media (--medium-plus) {
        
      }
      @media (--large) {
        
      }
      @media (--xlarge) {
        
      }
      @media (--xlarge-plus) {
      height: 455px;
      width: 209px;
      top: -37%;
      right: 36%;
        
    }
  }
}

 
</style>

