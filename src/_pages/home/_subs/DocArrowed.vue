<template>
    <div class="docArrowed">
        <p>Documentation
            <span class="rightArrow">
                <img src=/src/assets/objet-dynamique-vectoriel.png >
            </span>
        </p>
    </div>
</template>
<script>
export default {
}
</script>
<style>
.docArrowed {
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
