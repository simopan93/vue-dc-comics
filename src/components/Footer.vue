<template>
  
  <footer>
    <TopFooter />
    <BottomFooter />
  </footer>

</template>

<script>
import TopFooter from '../components/TopFooter';
import BottomFooter from '../components/BottomFooter';

export default {
  name: "Footer",

  components: {
    TopFooter,
    BottomFooter
  }
}
</script>

<style lang="scss">
@import "../assets/styles/vars.scss";
@import "../assets/styles/mixins.scss";


</style>