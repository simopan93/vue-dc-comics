<template>

  <header class="container">
    <img src="../assets/img/dc-logo.png">
    <ul>
      <li v-for="(item, index) in categories" :key="index"
      :class ="{active: item.current}">
        <a>{{item.name.toUpperCase()}}</a>
      </li>
    </ul>
  </header>

</template>

<script>
export default {
  name: "Header",
  data(){
    return{
      categories: [ 
        {
        name: "Characters",
        current: false,
      },
        {
        name: "Comics",
        current: true,
      },
        {
        name: "Movies",
        current: false,
      },
        {
        name: "TV",
        current: false,
      },
        {
        name: "Games",
        current: false,
      },
        {
        name: "Collectibles",
        current: false,
      },
        {
        name: "Videos",
        current: false,
      },
        {
        name: "Fans",
        current: false,
      },
        {
        name: "News",
        current: false,
      },
        {
        name: "Shop",
        current: false,
      },
        
      ]
    }
  }
}
</script>

<style lang="scss">

@import "../assets/styles/vars.scss";
@import "../assets/styles/mixins.scss";

header {
  @include center(align);
  justify-content: space-between;

  ul {
    display: flex;
    list-style: none;
  }

  li {
    margin: 0 10px;
    padding: 50px 0;
    transition: all 0.1s;
    &:hover,
    &.active{
      cursor: pointer;
      border-bottom: 4px solid $primary-color;
    }
  }
}  
</style>