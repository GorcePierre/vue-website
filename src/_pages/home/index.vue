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
        <section class="imgSmallLogo">
            <img src="/src/assets/logo.png" >
            <article class="headerTitle" >
                <h1>Code static websites<br>with VueJs powers.</h1>
            </article>
        </section>
        <div class="imgLogo">
            <img class="logo" src="/src/assets/2000px-Vue.svg.png">
            <div class="shadowBox"></div>
        </div>
        <section class= "editedBlock">
            <div class="blockBox">
                <article>
                    <h4 class ="titleBlock">NO MORE SPAGHETTI CODE</h4>
                    <p class = "textBlock"> Stop writing big files containing all code, no more<br> jQuery. Use simple declarative components.</p>
                </article>
                <aside class="pictureBlock">
                    <img src="/src/assets/firstArticlePicture.png" alt="first article picture">
                </aside>
                </div>
        </section>
        <section class= "editedBlock1">
            <div class="blockBox1">
                <article>
                    <h4 class ="titleBlock1">UNIFIED LANGUAGE</h4>
                    <p class = "textBlock1"> you don't need to code your site on the one hand<br> and use a static site generator on the second hand.<br> You code it once in components and it works.</p>
                </article>
                <aside class="pictureBlock1">
                    <img src="/src/assets/secondArticlePicture.png" alt="second article picture">
                </aside>
            </div>
        </section>
            <section class= "editedBlock2">
                <div class="blockBox2">
                    <article>
                        <h4 class ="titleBlock2">STATIC AND REACTIVE</h4>
                        <p class = "textBlock2"> Pages are static so they are fast and SEO ready. But<br> you benefit from single page applications features,<br> like html5 history navigation.</p>
                    </article>
                    <aside class="pictureBlock2">
                        <img src="/src/assets/thirdArticlePicture.png" alt="third article picture">
                    </aside>
                </div>
            </section>
        <div class= "imgBack">
            <section class = "imgFilter"> </section>
        </div>
    </div>
    <div class="bodyBlock">
        <section class="firstBackEffect"></section>
        <section class="secondBackEffect"></section>
        <section class="thirdBackEffect">
            <article class="subThirdEffect"></article>
        </section>
        <section class="docButton">
        <button>Documentation</button>
        </section>
    </div>
</div>
  
</template>
<script>
export default {
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
.imgBack {position:static;
    background-image: url(/src/assets/QDSMoAMTYaZoXpcwBjsL__DSC0104-1.jpg);
    height: 1850px;
    width: auto;
    margin: -1845px 0 0 -674px;
    background-repeat: no-repeat;
    background-size: cover;
    z-index: 0;
}
.imgFilter {
    position: relative;
    background-color: black;
    opacity: 0.6;
    height: 1850px;
    width: 100%;
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
    font-size: 58px;
    font-weight: bold;
}
.imgLogo {
    position: relative;
    margin-left: 41%;
    overflow: visible;
    z-index: 1;
}
.logo{
    position: absolute;
    bottom: -791px;
    margin-left: 24px;
    z-index: 1;
    object-fit: contain;
    width: 997px;
}
.shadowBox{
    position: absolute;
    top: -26px;
    left: -512px;
    height: 1976px;
    width: 867px;
    -webkit-transform: rotate(30deg);
    transform: rotate(30deg);
    background-color: #35495e;
    z-index: -1;
}
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
.docButton {
    position: relative;
    top: -97%;
    margin-left: 43%;
    z-index: 10;
}

button{
    padding: 20px 40px;
    border:5px solid #42b883;
    color: #42b883;
    background-color: transparent;
    font-weight: bold;
    font-size: 25px;
    border-radius: 2px;
    cursor: pointer;
}
button:hover{
    background-color:  #42b883;
    color:#202e3c
}

</style>


