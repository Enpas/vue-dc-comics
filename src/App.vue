<template>
  <div id="app">

    <Header />
    <Jumbotron />
    <Main />
    <Shop />
    <Footer />

  </div>
</template>

<script>

import Header from './components/Header.vue';
import Jumbotron from './components/Jumbotron.vue';
import Main from './components/Main.vue';
import Shop from './components/Shop.vue';
import Footer from './components/Footer.vue';


export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Main,
    Shop,
    Footer
    
  }
}
</script>

<style lang="scss">

  @import 'assets/style/global.scss';
  @import 'assets/style/utilities.scss';
 

</style>
