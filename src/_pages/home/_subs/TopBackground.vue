<template>
   <div class= "imgBack">
            <section class ="imgFilter"> </section>
        </div>
</template>
<script>
export default {

}
</script>
<style lang="postcss">
@import '../../../commons';
.imgBack {
    background-image: url(/src/assets/QDSMoAMTYaZoXpcwBjsL__DSC0104-1.jpg);
    position: relative;
    background-repeat: no-repeat;
    background-size: cover;
    z-index: 0;
    margin: -933px -855px 0px -452px;
    height: 626px;
        @media (--medium) {
            margin: -1231px -477px 0px -412px;
            height: 775px;
        }
        /* @media  (width >= 681px) and (width <= 831px) {
            margin: -1246px -477px 0px -412px;
            height: 776px;
        } */   
        @media (--medium-plus) {
            margin: -1649px -600px -71px -455px;
            height: 1000px;
        }
        @media (--large) {
            margin: -1822px -159px 0px -362px;
            height: 980px;
        }
        @media (--xlarge) {
            margin: -1995px 0px 0px -410px;
            height: 1270px;
        }
        @media (--xlarge-plus) {
            margin: -3175px 0px 0px -657px;
            height: 1758px; 
        }
    & .imgFilter {
        position: relative;
        background-color: var(--black-text);
        opacity: 0.6;
        height: 100%;
        width: 100%;
    }
}
</style>
