<template>
    <div class="imgSmallLogo">
        <img src="/src/assets/logo.png">
        <article class="headerTitle" >
            <h1>Code static websites<br>with VueJs powers.</h1>
        </article>
    </div>
</template>
<script>
export default {
}
</script>
<style lang="postcss">
@import '../../../commons';

.imgSmallLogo {
    position: relative;
    z-index: 2;
    top: 16px;
    left: 25px;
    width: 50px;
        @media  (width >= 425px) and (width < 531px) {
            top:15px;
        }
        @media (--medium) {
            top: 40px;
            left: 33px;
            width: 100px;            
        }
        @media  (width >= 681px) and (width <= 831px) {
          top:50px;
        }
        @media (--medium-plus) {
            top: 75px;
            left: 60px;
            width: 150px;            
        }
        @media (--large) {
            top: 110px;
            left: 70px;
            width: 185px;            
        }
        @media (--xlarge) {
            top: 536px;
            left: 90px;
            width: 250px;            
        }
        @media (--xlarge-plus) {
            top: 250px;
            left: 100px;
            width: 300px;
        }

& .headerTitle {
    position: absolute;
    overflow: visible;
    font-weight: bold;
    color: var(--white-text);
    z-index: 5;
    height: 70px;
    width: 249px;
    font-size: 16px;
        @media (--medium) {
            width: 264px;
            font-size: 17px;
        }
        @media (--medium-plus) {
            width: 508px;
            font-size: 29px;
        }
        @media (--large) {
            width: 490px;
            font-size: 33px;
        }
        @media (--xlarge) {
            width: 594px;
            font-size: 40px;
        }
        @media (--xlarge-plus) {
            width: 1000px;
            font-size: 48px;
        }
    }

    & img{
        width:100%
    }
}
</style>
