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
@import '../commons';
.docButton {
    position: relative;
    margin-bottom: 7%;
    
    z-index: 10;

    & button {
        padding: 20px 40px;
        border:5px solid var(--vue-green);
        color:var(--vue-green);
        background-color: transparent;
        font-weight: bold;
        font-size: 25px;
        border-radius: 2px;
        cursor: pointer;
    }

    & button:hover{
        background-color:  var(--vue-green);
        color: var(--dark-blue)
    }
}
</style>

