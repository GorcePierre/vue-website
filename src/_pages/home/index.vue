<template>
  <div class="main">
    <doc-arrowed></doc-arrowed>
    <img-small-logo></img-small-logo>
    <img-logo></img-logo>
    <top-background></top-background>
    <body-block></body-block>
    <block v-for="(block, index) of blocks" 
    :key="(block, index)" 
    :data="block" 
    @animated="startAnimation"
    @resetAnimated="resetAnimation" >
    </block>
    <button-vue-website :content="msg" class="docButton"></button-vue-website>
  </div>
</template>
<script>
import DocArrowed from './_subs/DocArrowed.vue'
import ImgSmallLogo from './_subs/ImgSmallLogo.vue'
import ImgLogo from './_subs/ImgLogo.vue'
import Block from './_subs/Block.vue'
import TopBackground from './_subs/TopBackground.vue'
import BodyBlock from './_subs/BodyBlock.vue'

export default {
  data () {
    return {
      msg: 'Documentation',
      blocks: [
        {
          title: 'NO MORE SPAGHETTI CODE',
          article:
            'Stop writing big files containing all code, no more jQuery.Use simple declarative components.',
          image: '/src/assets/firstArticlePicture.png',
          animatedImage: '/src/assets/animatedPicture1.png',
          spec: 'case1',
          isAnimated: false
        },
        {
          title: 'UNIFIED LANGUAGE',
          article:
            'You don\'t need to code your site on the one hand and use a static site generator on the second hand. You code it once in components and it works.',
          image: '/src/assets/secondArticlePicture.png',
          animatedImage: '/src/assets/animatedPicture2.png',
          spec: 'case2',
          isAnimated: false
        },
        {
          title: 'STATIC AND REACTIVE',
          article:
            'Pages are static so they are fast and SEO ready. But you benefit from single page applications features,\n like html5 history navigation.',
          image: '/src/assets/thirdArticlePicture.png',
          animatedImage: '/src/assets/animatedPicture3.png',
          spec: 'case3',
          isAnimated: false
        }
      ]
    }
  },
  components: {
    DocArrowed,
    ImgSmallLogo,
    ImgLogo,
    Block,
    TopBackground,
    BodyBlock
  },
  methods: {
    startAnimation () {
      if (window.scrollY > 300) {
        this.blocks[0].isAnimated = true
      }
      if (window.scrollY > 700) {
        this.blocks[1].isAnimated = true
      }
      if (window.scrollY > 1000) {
        this.blocks[2].isAnimated = true
      }
    },
    resetAnimation () {
      if (window.scrollY <= 300) {
        this.blocks[0].isAnimated = false
      }
      if (window.scrollY <= 700) {
        this.blocks[1].isAnimated = false
      }
      if (window.scrollY <= 1000) {
        this.blocks[2].isAnimated = false
      }
    }
  }
}
</script>
<style>
@import '../../commons';
.main {
  font-family: "Roboto", bold, Arial, Helvetica, sans-serif;
  margin-top: -8px;
  margin-right: -8px;
  margin-bottom: -8px;
  margin-left: -8px;
  max-height: 2500px;
  height: 100%;
  overflow: hidden;
      @media (--large) {
        max-height: 2000px;
      }
      @media (--xlarge) {
        margin-top: -381px;
        max-height: 2500px; 
      }
      @media (--xlarge-plus) {
        margin-top: -24px;  
      }
    & .docButton {
      margin-top: -228px;
      right: -13%;
      @media  (width >= 411px) and (width <= 530px) {
          right:-17%;
      }
      @media (--medium) {

        right: -25%;
      }
      @media  (width >= 681px) and (width <= 831px) {
          right:-30%;
      }
      @media (--medium-plus) {
          right:-33%;
      }
      @media (--large) {
        top:-1378px;
        right:-36%
      }
      @media (--xlarge) {
        right:-41% 
      }
      @media (--xlarge-plus) {
        top:-1278px
      }
  }

}
</style>