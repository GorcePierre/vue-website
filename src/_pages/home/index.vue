<template>
<div class="main">
    <div class= "headerBlock">
        <section class="docPath">
            <p>Documentation
                <span class="rightArrow">
                    <img src=/src/assets/objet-dynamique-vectoriel.png >
                </span>
            </p>
        </section>
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

import ImgSmallLogo from './_subs/ImgSmallLogo.vue'
import ImgLogo from './_subs/ImgLogo.vue'
import EditedBlock from './_subs/EditedBlock.vue'
import EditedBlock1 from './_subs/EditedBlock1.vue'
import EditedBlock2 from './_subs/EditedBlock2.vue'
import TopBackground from './_subs/TopBackground.vue'
import BodyBlock from './_subs/BodyBlock.vue'

export default {
  components: {
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
.docPath {
    position: relative;
    margin-left: 66px;
    margin-top: 30px;
    color: white;
    font-size: 20px;
    font-weight: bold;
    z-index: 1;
    cursor: pointer;
}
.rightArrow{
    position: absolute;
    margin-left: 10px;
}
</style>