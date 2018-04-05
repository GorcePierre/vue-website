<template>
    <div class= "editedBlock">
        <div class="blockBox">
            <article>
                <h4 class ="titleBlock">NO MORE SPAGHETTI CODE</h4>
                <p class = "textBlock"> Stop writing big files containing all code, no more<br> jQuery. Use simple declarative components.</p>
            </article>
            <aside class="pictureBlock">
                <img src="/src/assets/firstArticlePicture.png" alt="first article picture">
            </aside>
        </div>
    </div>
</template>
<script>
export default {
}
</script>
<style>
.editedBlock {
    position: relative;
    border-bottom: 7px solid White;
    height: 354px;
    width: 1000px;
    top: 973px;
    right: -20%;
    color: white;
    z-index: 5;
    text-align: center;
}
.blockBox {
    margin-left: 25%;
    border-top: 7px solid White;
}
.titleBlock {
    position: absolute;
    top:5%;
    font-size: 35px;
    right: 50%;
}
.textBlock {
    position: absolute;
    font-size: 25px;
    top:40%;
    font-weight: bold;
    margin-left: -28%
}
.pictureBlock {
    position: relative;
    background-color: white;
    float: right;
    height: 100%;
    width: 300px;
    padding: 60px 30px 60px 30px;
}

</style>

