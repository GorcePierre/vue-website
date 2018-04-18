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
export default {}
</script>
<style lang="postcss">
@import '../../../commons';
.docArrowed {
  position: relative;
  color:var(--white-text);
  font-weight: bold;
  z-index: 1;
  cursor: pointer;
  top: 10px;
  margin-left: 21px;
  font-size: 10px;
  
    @media (--medium) {
        top: 12px;
        margin-left: 30px;
        font-size: 14px;
    }
    @media (--medium-plus) {
        top: 14px;
        margin-left: 35px;
        font-size: 16px;
    }
    @media (--large) {
        top: 16px;
        margin-left: 40px;
        font-size: 18px;
    }
    @media (--xlarge) {
        top: 388px;
        margin-left: 45px;
        font-size: 24px;
    }
    @media (--xlarge-plus) {
        top: 20px;
        margin-left: 50px;
        font-size: 28px;
    }
    
  & .rightArrow {
    position: absolute;
    margin-left: 10px;
    bottom: -7px;

        @media (--medium) {
            bottom: -5px; 
        }
  }
}
</style>
