<template>

  <div class="productCard">
    <img :src="comic.thumb" :alt="comic.series">
    <h5>{{comic.series.toUpperCase()}}</h5>
  </div>
  
</template>

<script>
export default {  
  name: "ProductCard",
  props:{
    comic: Object,
  }

}
</script>



<style lang="scss">

@import "../assets/styles/vars.scss";
@import "../assets/styles/mixins.scss";


.productCard {
  width: calc(100% / 6);
  height: 50%;
  padding: 20px 15px;

  h5{
    font-weight: initial;
    color: gray;
  }

  img{
    width: 100%;
    height: 90%;
    transition: all 0.5s;

    &:hover{
      cursor: pointer;
      filter: brightness(1.3);
      border: 1px solid gold;
    } 
  }

  

  
}
</style>