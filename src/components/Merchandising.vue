<template>
  
  <section class="merchandising">
    <div class="container">
      <div v-for="(item,index) in ListMercha"
      :key="index"
      class="slot">
        <a>
          <img :src="item.logo" :alt="item.name">
          <span>{{item.name.toUpperCase()}}</span>
        </a>
      </div>
    </div>
  </section>

</template>

<script>

import ListMercha from "../assets/data/ListMerchandising.js"

export default {
  name: "Merchandising",

  data(){
    return{
      ListMercha,
    }
  }
}
</script>

<style lang="scss">

@import "../assets/styles/vars.scss";
@import "../assets/styles/mixins.scss";

.merchandising {
  background-color: $primary-color;

  .container{
    @include center();
    padding: 30px 0;
  }

  .slot {
    width: calc(100% / 5);
    min-width: 170px;
    height: 50px;
    color: white;

    a{
      @include center();
      height: 100%;

      &:hover{
        cursor: pointer;
        color: lightgray;
      }


      img {
        width: 20%;
        height: 100%;
      }

      span{
        margin: 0 10px;
      }


    }

    
  }
}

</style>