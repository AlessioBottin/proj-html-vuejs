<template>
  <div id="app">
    <Header />
    
    <FloatingButtons />

    <Main />

    <Footer />
  </div>
</template>

<script>
import "@fontsource/work-sans";
import "@fontsource/source-serif-pro";
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import FloatingButtons from "./components/FloatingButtons.vue";


export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
    FloatingButtons
  },
};
</script>

<style lang="scss">
@import './styles/general.scss';

</style>
