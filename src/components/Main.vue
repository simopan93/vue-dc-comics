<template>
  
  <main>
    <div class="bg-image"></div>
    <div class="container">
      <button>CURRENT SERIES</button>
      <ProductCard 
      v-for="(item,index) in ListComics"
      :key="index"
      :comic="item"
      />
    </div>
  </main>

</template>

<script>
import ProductCard from "./ProductCard";
import ListComics from "../assets/data/productData.js";


export default {
  name: "Main",

  components: {
    ProductCard
  },
  
  data()
  {
    return{
      ListComics,
    }
  }
}
</script>



<style lang="scss">
  @import "../assets/styles/mixins.scss";
  @import "../assets/styles/vars.scss";

  main {
    background-color: black;
    color: white;

    .bg-image {
      height: 250px;
      background-image: url(../assets/img/jumbotron.jpg);
      background-size: cover;
      background-repeat: no-repeat;
    }

    

    .container{
      position: relative;
      @include center(align);
      flex-wrap: wrap;
      height: 450px;
      padding: 20px 0;


        button {
        position: absolute;
        top: -20px;
        left: 0;
        color: white;
        font-size: 1.1rem;
        background-color: $primary-color;
        padding: 10px 15px;
        border: none;
        border-radius: 0;

        &:hover{
          cursor:pointer;
        }
    }
    }
  }
</style>