<template>
  <section class="bottom-footer">
    <div class="container">

      <button>SIGN-UP NOW</button>

      <div class="box-social">
        <a>FOLLOW US</a>
        <div v-for="(item,index) in Social"
        :key="index" 
        class="box-logo">

          <img :src="item.logo" alt="item.social">
        
        </div>

      </div>
    </div>
    

  </section>
  
</template>





<script>
import Social from "../assets/data/ListSocial.js"



export default {
   name: "BottomFooter",


    data() {
      return{
        Social
      }
    }
}
</script>





<style  lang="scss">
  @import "../assets/styles/vars.scss";
  @import "../assets/styles/mixins.scss";




  .bottom-footer {
    height: 80px;
    background-color: #303030;

    .container{
      @include center(align);
      justify-content: space-between;
      height: 100%;



      button {
        color: white;
        font-size: 15px;
        border: 2px solid $primary-color;
        background-color: #303030;
        padding: 10px;

        &:hover{
          cursor: pointer;
          color: lightgray;
        }
      }

      .box-social{
        @include center();


        a {
          color: $primary-color;
          margin-right: 15px;


          &:hover {
            cursor: pointer;
          }
        }

        img {
          margin: 0 10px;
          transition: background-color 0.2s;
          transition: border-radius 0s;


          &:hover {
            cursor: pointer;
            background-color: white;
            border-radius: 50%;
          }
        }
      }
    }

    
  }
</style>