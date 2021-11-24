<template>
  
  <section class="merchandising">
    <div class="container">
      <div v-for="(item,index) in options"
      :key="index"
      class="slot">
        <img src="../assets/img/buy-comics-digital-comics.png" alt="">
        <span>{{item.name.toUpperCase()}}</span>
      </div>
    </div>
  </section>

</template>

<script>
export default {
  name: "Merchandising",
  data(){
    return{
      options: [
        {
          name: "Digital Comics",
          logo: "buy-comics-digital-comics.png"
        },
        {
          name: "DC Merchandise",
          logo: "buy-comics-merchandise.png"
        },
        {
          name: "Subscription",
          logo: "buy-comics-subscriptions.png"
        },
        {
          name: "Comic Shop Locator",
          logo: "buy-comics-shop-locator.png"
        },
        {
          name: "DC Power Visa",
          logo: "buy-dc-power-visa.svg"
        },
      ]
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
    @include center();
    width: calc(100% / 5);
    min-width: 170px;
    color: white;

  img {
    width: 20%;
  }

    span{
      margin: 0 10px;
    }
  }
}

</style>