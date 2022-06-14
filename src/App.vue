<template>
  <div id="app">
    <main class="content-main">
      <router-view/>
    </main>
    <Footer/>
  </div>
</template>
<script>
import Footer from './components/footer/Footer.vue';

export default {
  components: {
    Footer
  }
}
</script>

<style lang="scss">
@import './assets/scss/generic/mixins.scss';
@import './assets/scss/generic/fonts.scss';

$bg-default: #FFF4FE;
$black: #000;
$white: #fff;
$ligthgray: #D9D9D9;
$gray: #958F8F;
$darkgray: #5d5d60;
$purple: #740DCE;

#app {
  font-family: 'Roboto', sans-serif;
  min-height: 100vh;
  background-color: $bg-default;
}

body {
  margin: 0;
  width: 100%;
  color: #687188;
  overflow: hidden;
}

</style>
