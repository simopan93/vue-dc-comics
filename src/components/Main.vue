<template>
  
  <main>
    <div class="container">
      <h1>-->Content Goes Here</h1>
    </div>
  </main>

</template>

<script>
export default {
  name: "Main"
}
</script>



<style lang="scss">
  @import "../assets/styles/mixins.scss";

  main {
    height: 200px; //Da Togliere?
    background-color: black;
    color: white;

    .container{
      @include center(align);
      height: 100%; //Da Togliere
    }
  }
</style>