<template>
<div class="main">
    <div class= "headerBlock">
        <doc-arrowed></doc-arrowed>
        <img-small-logo></img-small-logo>
        <img-logo></img-logo>
        <edited-block></edited-block>
        <edited-block1></edited-block1>
        <edited-block2></edited-block2>
        <top-background></top-background>
    </div>
    <body-block></body-block>
</div>
  
</template>
<script>

import DocArrowed from './_subs/DocArrowed.vue'
import ImgSmallLogo from './_subs/ImgSmallLogo.vue'
import ImgLogo from './_subs/ImgLogo.vue'
import EditedBlock from './_subs/EditedBlock.vue'
import EditedBlock1 from './_subs/EditedBlock1.vue'
import EditedBlock2 from './_subs/EditedBlock2.vue'
import TopBackground from './_subs/TopBackground.vue'
import BodyBlock from './_subs/BodyBlock.vue'

export default {
  components: {
    DocArrowed,
    ImgSmallLogo,
    ImgLogo,
    EditedBlock,
    EditedBlock1,
    EditedBlock2,
    TopBackground,
    BodyBlock
  }
}
</script>
<style>
.main {
    font-family: "Roboto",bold, Arial, Helvetica, sans-serif;
    display: block;
    margin-top: 0px;
    margin-right: -8px;
    margin-bottom: 0px;
    margin-left: -8px;
    height: 100vh;
    width: 99vw;
    max-width: 101%;
    min-width: 100%;

}
.headerBlock {
    position: relative;
    width: auto;
}
</style>