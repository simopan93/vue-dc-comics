<template>
  <body>
    <Header />
    <Main />
    <Merchandising />
    <Footer />
  </body>
</template>

<script>
import Header from '../src/components/Header';
import Main from '../src/components/Main';
import Merchandising from '../src/components/Merchandising';
import Footer from '../src/components/Footer';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Merchandising,
    Footer
  }
}
</script>

<style lang="scss">
@import "./assets/styles/general.scss";
@import "./assets/styles/utilities.scss";
@import "./assets/styles/vars.scss";


</style>
