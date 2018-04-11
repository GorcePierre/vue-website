<template>
    <div class="docButton">
        <button>{{content}}</button>
    </div>
</template>
<script>
export default {
  props: {
    type: String,
    content: ''
  }
}
</script>
<style>
.docButton {
    position: relative;
    margin-bottom: 7%;
    margin-left: 43%;
    z-index: 10;
}

button {
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

