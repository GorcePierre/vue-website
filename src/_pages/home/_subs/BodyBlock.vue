<template>
    <div class="bodyBlock">
        <section class="firstBackEffect"></section>
        <section class="secondBackEffect"></section>
        <section class="thirdBackEffect">
            <article class="subThirdEffect"></article>
        </section>
    <button-vue-website></button-vue-website>
    </div>
</template>
<script>
export default {
}
</script>
<style >
.bodyBlock{
    position: relative;
    overflow: hidden;
    background-color: #35495e;
    height: 1450px; 
    width: 100%;
    z-index: -3;

}
.firstBackEffect {
    position: relative;
    background-color: #202e3c;
    height: 415px;
    width: 500px;
    z-index: 0;
    opacity: 0.6;
}
.secondBackEffect {
    position: relative;
    background-color: #202e3c;
    height: 1605px;
    width: 500px;
    left: 1470px;
    top: -335px;
    -webkit-transform: rotate(30deg);
    transform: rotate(30deg);
    z-index: 0;
    opacity: 0.6;
}
.thirdBackEffect {
    position: relative;
    background-color: #202e3c;
    transform: rotate(30deg);
    z-index: 0;
    top: -72%;
    height: 43%;
    width: 15%;
    right: -28.2%;
}
.subThirdEffect{
    position: absolute;
    background-color: #35495e;
    height: 455px;
    width: 209px;
    -webkit-transform: rotate(60deg);
    transform: rotate(60deg);
    top: -37%;
    right: 36%;
}
</style>

