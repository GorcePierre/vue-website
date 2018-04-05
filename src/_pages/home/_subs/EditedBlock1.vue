<template>
    <div class= "editedBlock1">
        <div class="blockBox1">
            <article>
                <h4 class ="titleBlock1">UNIFIED LANGUAGE</h4>
                <p class = "textBlock1"> you don't need to code your site on the one hand<br> and use a static site generator on the second hand.<br> You code it once in components and it works.</p>
            </article>
            <aside class="pictureBlock1">
                <img src="/src/assets/secondArticlePicture.png" alt="second article picture">
            </aside>
        </div>
    </div>
</template>
<script>
export default {
}
</script>
<style>
.editedBlock1 {
    position: relative;
    border-top: 7px solid White;
    height: 350px;
    width: 1000px;
    top: 1025px;
    right: -28%;
    color: white;
    z-index: 5;
    text-align: center;
}
.blockBox1 {
    height: 100%;
    border-bottom: 7px solid White;
    width: 75%
}
.titleBlock1 {
    position: absolute;
    top:5%;
    font-size: 35px;
    text-align: center;
    margin-left: 53%;
}
.textBlock1 {
    position: absolute;
    font-size: 25px;
    top:40%;
    font-weight: bold;
    margin-left: 40%;
    right: -3%
}
.pictureBlock1 {
    position: relative;
    background-color: white;
    float: left;
    height: 59%;
    width: 300px;
    padding: 75px 30px 75px 20px;
}

</style>


