<template>
<div class= "editedBlock2">
    <div class="blockBox2">
        <article>
            <h4 class ="titleBlock2">STATIC AND REACTIVE</h4>
            <p class = "textBlock2"> Pages are static so they are fast and SEO ready. But<br> you benefit from single page applications features,<br> like html5 history navigation.</p>
        </article>
        <aside class="pictureBlock2">
            <img src="/src/assets/thirdArticlePicture.png" alt="third article picture">
        </aside>
    </div>
</div>
</template>
<script>
export default {

}
</script>
<style>
.editedBlock2 {
    position: relative;
    border-top: 7px solid White;
    height: 350px;
    width: 1000px;
    top: 1085px;
    right: -20%;
    color: white;
    z-index: 5;
    text-align: center;
}
.blockBox2 {
    height: 100%;
    border-bottom: 7px solid White;
    width: 75%;
    margin-left: 25%
    
}
.titleBlock2 {
    position: absolute;
    top:5%;
    font-size: 35px;
    right: 53%;
}
.textBlock2 {
    position: absolute;
    font-size: 25px;
    top:40%;
    font-weight: bold;
    margin-left: -30%;
}
.pictureBlock2 {
    position: relative;
    background-color: white;
    float: right;
    height: 50%;
    width: 300px;
    padding: 90px 30px 90px 30px;
    z-index: 2;
}

</style>
