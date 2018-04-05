<template>
    <div class="imgSmallLogo">
        <img src="/src/assets/logo.png" >
        <article class="headerTitle" >
            <h1>Code static websites<br>with VueJs powers.</h1>
        </article>
    </div>
</template>
<script>
export default {
}
</script>
<style>
.imgSmallLogo {
    position: absolute;
    top: 270px;   
    left: 100px;
    height: 200px;
    width: 200px;
    z-index: 2;
}
.headerTitle {
    position: absolute;
    color: white;
    z-index: 5;
    overflow: visible;
    height: 350px;
    width: 1000px;
    font-size: 48px;
    font-weight: bold;
}
</style>
