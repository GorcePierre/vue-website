<template>
    <div class= "editedBlock" :class="[data.style]">
        <div class="blockBox" :class="[data.style]">
            <article>
                <h4 class ="titleBlock" :class="[ data.position ]">{{data.title}}</h4>
                <p class = "textBlock" :class="[ data.position ]"> {{data.article}}</p>
            </article>
            <aside class="pictureBlock" :class="[ data.position, data.style ]" >
                <img :src='data.image'>
            </aside>
        </div>
    </div>
</template>
<script>
export default {
  props: {
    data: {
      type: Object,
      default () {
        return {
          title: '',
          article: '',
          image: '',
          animatedImage: '',
          position: ''
        }
      }
    }
  }
}
</script>
<style>
.editedBlock {
    position: relative;
    margin-top: 75px;
    height: 354px;
    width: 1000px;
    top: -1660px;
    right: -20%;
    color: white;
    z-index: 5;
    text-align: center;

        &.case1 {
      border-bottom: 7px solid White        
        }
        &.case2 {
      border-bottom: 7px solid White;
        }
        &.case3 {
      border-top: 7px solid White;
        }

    & .blockBox {

            &.case1 {
            margin-left: 25%;
            border-top: 7px solid White;
            }
            &.case2 {
                height: 100%;
                border-top: 7px solid White;
                width: 75%
            }
            &.case3 {
                height: 100%;
                margin-left: 25%;
                border-bottom: 7px solid White;
            }

        & .titleBlock {
            position: absolute;
            top:5%;
            font-size: 35px;
            
                &.left{
                    left: 65%;
                }
                &.right{
                    right: 50%;
                }
            }
        & .textBlock {
            word-wrap:break-word;
            width: 67%;
            position: absolute;
            font-size: 25px;
            top:40%;
            font-weight: bold;
            margin-left: -28%;

              &.left{
                  right: -5%
               }
              &.right{
                  right: 40%;
              }
            }
        & .pictureBlock {
            position: relative;
            background-color: white;
            height: 100%;
            width: 300px;

            &.left{
                height: auto;
                float: left;
                padding: 75px 30px 75px 30px;
            }
            &.right{
                float: right;
                padding: 60px 30px 60px 30px;
            }
            &.case3{
                padding: 0px 30px 0px 30px;

                & img{
                 padding: 81px 0px 0px 0px;
                }
            }
        }
    }
}

</style>
