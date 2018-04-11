<template>
  <div class="main">
    <doc-arrowed></doc-arrowed>
    <img-small-logo></img-small-logo>
    <img-logo></img-logo>
    <top-background></top-background>
    <body-block></body-block>
    <block v-for="(block, index) of blocks" :key="(block, index)" :data="block" ></block>
    <button-vue-website :content="msg" class="docButton" ></button-vue-website>
  </div>
</template>
<script>
import DocArrowed from "./_subs/DocArrowed.vue";
import ImgSmallLogo from "./_subs/ImgSmallLogo.vue";
import ImgLogo from "./_subs/ImgLogo.vue";
import Block from "./_subs/Block.vue";
import TopBackground from "./_subs/TopBackground.vue";
import BodyBlock from "./_subs/BodyBlock.vue";

export default {
  data() {
    return {
      msg: "Documentation",
      blocks: [
        {
          title: "NO MORE SPAGHETTI CODE",
          article:
            "Stop writing big files containing all code, no more jQuery.Use simple declarative components.",
          image: "/src/assets/firstArticlePicture.png",
          animatedImage: "/src/assets/firstArticlePicture.png",
          position: "right",
          style: "case1"
        },
        {
          title: "UNIFIED LANGUAGE",
          article:
            "You don't need to code your site on the one hand and use a static site generator on the second hand. You code it once in components and it works.",
          image: "/src/assets/secondArticlePicture.png",
          animatedImage: "/src/assets/secondArticlePicture.png",
          position: "left",
          style: "case2"
        },
        {
          title: "STATIC AND REACTIVE",
          article:
            "Pages are static so they are fast and SEO ready. But you benefit from single page applications features,\n like html5 history navigation.",
          image: "/src/assets/thirdArticlePicture.png",
          animatedImage: "/src/assets/thirdArticlePicture.png",
          position: "right",
          style: "case3"
        }
      ]
    };
  },
  components: {
    DocArrowed,
    ImgSmallLogo,
    ImgLogo,
    Block,
    TopBackground,
    BodyBlock
  }
};
</script>
<style>
.main {
  font-family: "Roboto", bold, Arial, Helvetica, sans-serif;
  margin-top: 0px;
  margin-right: -8px;
  margin-bottom: 0px;
  margin-left: -8px;
  max-height: 2500px;
  height: 100%;
  overflow: hidden;

}

.docButton {
  margin-top: -1500px;
}
</style>