<template>
    <div class= "editedBlock" :class="[data.style]">
        <div class="blockBox" :class="[data.style]">
            <article class="mobileBorder" :class="[data.style]">
                <h4 class ="titleBlock" :class="[data.style]">{{data.title}}</h4>
                <p class = "textBlock" :class="[data.style]"> {{data.article}}</p>
                <div class="mobileBottomBorder" :class="[data.style]"></div>
            </article>
            <aside class="pictureBlock" :class="[data.style ]" >
                <img :src='data.image'>
            </aside>
        </div>
    </div>
</template>
<script>
export default {
  props: {
    data: {
      type: Object,
      default () {
        return {
          title: '',
          article: '',
          image: '',
          animatedImage: '',
          data: ''
        }
      }
    }
  }
}
</script>
<style lang="postcss">
@import '../../../commons';

 .mobileBorder {
            position: absolute;
            height: 194px;
            width: 313px;
    @media (width < 1024px) {
        &.case1{
            top: 305px;
            right: -6px;
            border-right:7px solid var(--color-border);
        }
        &.case2{
            top:786px;
            right:-7.25px;
            border-left:7px solid var(--color-border);
        }
        &.case3{
            top: 1265px;
            right: -6px;
            border-right:7px solid var(--color-border);
        }
    }
        & .mobileBottomBorder{
                position: relative;
                width: 75%;
            @media (width < 1024px) {
            &.case1{
                height: 187px;
                border-bottom: 7px solid #FFFFFF;
                right: -85px;
            }
            &.case2{
                height: 193px;
                border-bottom: 7px solid #FFFFFF;
                right:7px;
            }
            &.case3{
                height: 187px;
                border-bottom: 7px solid #FFFFFF;
                right:-85px;
            }
            }
        }
}  
.editedBlock {
    position: relative;
    color: var(--white-text);
    z-index: 5;
    text-align: center;
    margin-top: 12px;
    height: 32px;
    width: 166px;
    top: -1785px;
    right: -47%;
        @media (width < 1024px) and (width >= 604px) {

            top: -1750px;
        }
        @media (--large) {    
            margin-top: 75px;
            height: 319px;
            width: 795px;
            right: -9%;
        }
        @media (--xlarge) {    
            margin-top: 75px;
            height: 319px;
            width: 999px;
            top: -1679px;
            right: -15%; 
        }
        @media (--xlarge-plus) {    
            margin-top: 75px;
            height: 319px;
            width: 1000px;
            top: -1660px;
            right: -20%; 
        }
        @media (width >= 1024px){
                &.case1, &.case2{
                    border-bottom: 7px solid var(--color-border);       
                }
                &.case3 {
                    border-top: 7px solid var(--color-border) ;
                }
    }
    & .blockBox {
        @media (width >= 1024px){
             &.case1 {
                 border-top: 7px solid var(--color-border);
             }   
        }
            &.case1 {
                margin-left: 25%;           
            }
            &.case2 {
                border-top: 7px solid var(--color-border);
                height: 100%;
                width: 75%;
            }
            &.case3 {
                height: 100%;
                margin-left: 25%;
                    @media (width >= 1024px){
                        border-bottom: 7px solid var(--color-border)
                    }    
            }
        & .titleBlock {
            position: absolute;
            font-size: 35px;
                &.case1{
                    right:16%;
                    font-size: 20px;
                    width: 202px;
                    @media (--large) {
                        top:10%;
                        right:24%;
                        font-size: 28px;
                        width: 486px;                    
                    }
                    @media (--xlarge) {
                        top:5%;
                        font-size: 35px;                    
                    }
                }
                &.case2{
                    right:15%;
                    font-size: 20px;
                    width: 226px;
                    @media (--large) {
                        right:-150%;
                        top:10%;
                        font-size: 28px; 
                        width: 350px;                   
                    }
                    @media (--xlarge) {
                        right:-180%;
                        top:5%;
                        font-size: 35px;                    
                    }
                }
                &.case3{
                    right:10%;
                    font-size: 20px;
                    width: 226px;
                    @media (--large) {
                        top:10%;
                        right:40%;
                        font-size: 28px;
                        width: 486px;                   
                    }
                    @media (--xlarge) {
                        top:5%;
                        font-size: 35px;                    
                    }
                }
            }
        & .textBlock {
            word-wrap:break-word;
            font-weight: bold;
            position: absolute;
            margin-left: -28%;
            width: 67%;
            font-size: 25px;
            top:40%;
            &.case1 {
                width: 77%;
                font-size: 17px;
                margin-left: 14%;
                top:36%;
                @media (--large) {
                    width: 155%;
                    font-size: 20px;
                    margin-left: 14%;
                    top:70%;
                    right: 19%;  
                }
                @media (--xlarge) {
                    width: 179%;
                    font-size: 22px;
                    margin-left: 14%;
                    top:66%;
                    right: 17%;   
                }
                @media (--xlarge-plus) {
                    width: 184%;
                    font-size: 24px;
                    margin-left: 14%;
                    top:66%;
                    right: 10%;
                }
            }
            &.case2 {
                width: 89%;
                font-size: 17px;
                margin-left: 5%;
                top:26%;
                @media (--large) {
                    width: 160%;
                    font-size: 20px;
                    margin-left:112%;
                    top:66%;    
                }
                @media (--xlarge) {
                    width: 177%;
                    font-size: 22px;
                    right:-231%;    
                }
                @media (--xlarge-plus) {
                    width: 189%;
                    font-size: 24px;
                    right:-231%;    
                }
            }
            &.case3 {
                margin-left: 7%;
                width: 88%;
                font-size: 17px;
                top:25%;
                @media (--large) {
                    width: 155%;
                    margin-left: 14%;
                    font-size: 20px;
                    top:70%;
                    right: 19%;    
                }
                @media (--xlarge) {
                    width: 186%;
                    font-size: 22px;
                    right:4%;
                }
                @media (--xlarge-plus) {
                    width: 192%;
                    font-size: 24px;
                    right:4%;   
                }
            }  
        }
        & .pictureBlock {
            position: relative;
            background-color: var(--color-border);
            width: 192px;
                @media (--xlarge-plus) {
                    width: 300px;
                }
            &.case1 {
                top: 10px;
                left: -153%;
                padding: 44px 103px 25px 26px;
                @media (--large) {
                    top:0px;
                    left: 46%;
                    padding: 55px 104px 25px 26px;    
                }
                @media (--xlarge) {
                    left: 57%;    
                }
                @media (--xlarge-plus) {
                    padding: 55px 20px 25px 26px;
                    left:53.80%
                }
            }
            &.case2 {
                height: auto;
                top: 1515%;
                left: -118%;
                padding: 46px 124px 48px 1px;
                @media (--large) {
                    top: 0%;
                    left: 0%;
                    padding: 56px 124px 56px 1px;    
                }
                @media (--xlarge) {
                    padding: 56px 130px 56px 10px;    
                }
                @media (--xlarge-plus) {
                    padding: 56px 30px 56px 20px;   
                }
            }
            &.case3{
                top: 3051%;
                left:-152%;
                padding: 64px 102px 64px 26px;
                @media (--large) {
                    top:0px;
                    left: 46%;
                    padding: 75px 104px 75px 26px;    
                }
                @media (--xlarge) {
                    left: 57%;    
                }
                @media (--xlarge-plus) {
                    left:52%;
                    padding: 75px 34px 75px 26px;
                }
            }
        }
    }
}

</style>
