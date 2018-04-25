<template>
    <div class= "editedBlock" :class="[data.spec]">
        <div class="blockBox" :class="[data.spec]">
            <article class="mobileBorder" :class="[data.spec]">
                <h4 class ="titleBlock" :class="[data.spec]">{{data.title}}</h4>
                <p class = "textBlock" :class="[data.spec]"> {{data.article}}</p>
                <div class="mobileBottomBorder" :class="[data.spec]"></div>
            </article>
            <transition-group
            name="reversePicture"
            @enter="resetAnimation"
            @after-leave="endResetAnimation"
            tag="aside"
            >
                <aside class="pictureBlock" :key='data.isAnimated' :class="!data.isAnimated ? [data.spec]: null" >
                    <img :src='data.image' v-if="!data.isAnimated">
	        </aside>
            </transition-group>
            <transition-group
            name="slidingPicture"
            @enter="enter"
            @after-leave="afterLeave"
            tag="aside">
                <aside class="animatedPictureBlock" :key='data.isAnimated' :class="data.isAnimated ? [data.spec]: null" >
                    <img :src='data.animatedImage' v-if="data.isAnimated">
            </aside>
            </transition-group>
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
          spec: '',
          isAnimated: ''
        }
      }
    }
  },
  methods: {
    enter () {
      this.$emit('animated')
    },
    afterLeave () {
      this.resetAnimation()
    },
    resetAnimation (el) {
      window.addEventListener('scroll', this.endResetAnimation)
    },
    endResetAnimation () {
      this.$emit('resetAnimated')
    }
  },
  created () {
    window.addEventListener('scroll', this.enter)
  },
  destroyed () {
    window.removeEventListener('scroll', this.enter)
    window.removeEventListener('scroll', this.endResetAnimation)
  }
}
</script>
<style lang="postcss">
@import '../../../commons';
 .slidingPicture-enter, .slidingPicture-leave-to {
     opacity:0;
 }
 .slidingPicture-enter-active {
     animation: rotateIn 1s ;
     opacity: 1;
 }
 .slidingPicture-leave-active{
     display:none
 }
 .reversePicture-enter, .reversePicture-leave-to{
     opacity: 1;
 }
 .reversePicture-enter-active {
     animation: slideInUp 0.5s
 }
 .reversePicture-leave-active{
     display:none;
 }
@-webkit-keyframes rotateIn {
  from {
    -webkit-transform-origin: center;
    transform-origin: center;
    -webkit-transform: rotate3d(0, 0, 1, -200deg);
    transform: rotate3d(0, 0, 1, -200deg);
    opacity: 0;
  }

  to {
    -webkit-transform-origin: center;
    transform-origin: center;
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    opacity: 1;
  }
}
@keyframes rotateIn {
  from {
    -webkit-transform-origin: center;
    transform-origin: center;
    -webkit-transform: rotate3d(0, 0, 1, -200deg);
    transform: rotate3d(0, 0, 1, -200deg);
    opacity: 0;
  }

  to {
    -webkit-transform-origin: center;
    transform-origin: center;
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    opacity: 1;
  }
}
@-webkit-keyframes slideInUp {
  from {
    -webkit-transform: translate3d(0, 100%, 0);
    transform: translate3d(0, 100%, 0);
    visibility: visible;
  }

  to {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }
}

@keyframes slideInUp {
  from {
    -webkit-transform: translate3d(0, 100%, 0);
    transform: translate3d(0, 100%, 0);
    visibility: visible;
  }

  to {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }
}

.editedBlock {
    position: relative;
    color: var(--white-text);
    z-index: 5;
    text-align: center;
    height: 32px;
    width: 166px;
    top: -1785px;
    right: -47%;
        @media (width >= 604px) and (width <= 1024px)  {
            top: -1750px;
        }
        @media (--large) {    
            margin-top: 75px;
            height: 319px;
            width: 795px;
            top: -1716px;
            right: -11%;
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
             &.case1, &.case2 {
                 border-top: 7px solid var(--color-border);
             }   
        }
            &.case1 {
                margin-left: 25%;           
            }
            &.case2 {
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
        & .mobileBorder {
            position: absolute;
            width: 313px;
                @media (width < 1024px) {
                    &.case1{
                        top: 305px;
                        right: -6px;
                        border-right:7px solid var(--color-border);
                    }
                    &.case2{
                        top:780px;
                        right:-7.25px;
                        border-left:7px solid var(--color-border);
                            &.animatedPictureBlock {
                                top:300px
                            }
                    }
                    &.case3{
                        top: 1277px;
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
                            border-bottom: 7px solid var(--color-border);
                            right: -85px;
                        }
                        &.case2{
                            height: 193px;
                            border-bottom: 7px solid var(--color-border);
                            right:7px;
                        }
                        &.case3{
                            height: 187px;
                            border-bottom: 7px solid var(--color-border);
                            right:-85px;
                        }
                    }
                }
            }
        & .titleBlock {
            position: absolute;
            font-size: 18px;
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
            margin-top:23%;
            &.case1 {
                width: 77%;
                font-size: 17px;
                margin-left: 14%;
                @media (--large) {
                    margin-top:45%;
                    width: 155%;
                    font-size: 20px;
                    margin-left: 14%;
                    right: 19%;  
                }
                @media (--xlarge) {
                    width: 179%;
                    font-size: 22px;
                    margin-left: 14%;
                    right: 17%;   
                }
                @media (--xlarge-plus) {
                    width: 184%;
                    font-size: 24px;
                    margin-left: 14%;
                    right: 10%;
                }
            }
            &.case2 {
                width: 89%;
                font-size: 17px;
                margin-left: 5%;
                @media (--large) {
                    margin-top:45%;
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
                @media (--large) {
                    margin-top:45%;
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
                bottom: -489px;
                left: -118%;
                padding: 46px 124px 48px 1px;
                @media (--large) {
                    top:-1px;
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
                bottom:-982px;
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
        & .animatedPictureBlock {
            position: relative;
            background-color: var(--color-border);
            width: 192px;
                @media (--xlarge-plus) {
                    width: 300px;
                }
            &.case1 {
                top: 12px;
                left: -153%;
                padding: 52px 126px 14px 3px;
                @media (--large) {
                    top:-6px;
                    left: 45%;
                    padding: 73px 130px 21px 6px;    
                }
                @media (--xlarge) {
                    padding: 73px 126px 21px 4px;    
                    left: 57%;    
                }
                @media (--xlarge-plus) {
                    padding: 73px 29px 21px 18px;
                    left:53.80%
                }
            } 
            &.case2 {
                top: 495px;
                left: -118%;
                padding: 67px 115px 49px 12px;
                @media (--large) {
                    margin-top: -2px;
                    top: -37%;
                    left: 0%;
                    padding: 75px 123px 58px 20px;    
                }
                @media (--xlarge) { 
                }
                @media (--xlarge-plus) {
                    padding: 76px 32px 58px 20px;    
                }
            }
            &.case3{
                top:988px;
                left: -152%;
                padding: 64px 110px 33px 18px;
                @media (--large) {
                    top: -6px;
                    left: 46%;
                    padding: 72px 113px 63px 18px    
                }
                @media (--xlarge) {
                    left: 57%;    
                }
                @media (--xlarge-plus) {
                    left:52%;
                    padding: 75px 34px 61px 26px;
                }
            }
        }
    }
}
</style>