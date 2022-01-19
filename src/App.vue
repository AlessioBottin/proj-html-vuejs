<template>
  <div id="app">
    <Header :menuLinksArray="menuLinks"/>
    
    <FloatingButtons />

    <Main />

    <Footer :menuLinksArray="menuLinks"/>
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
  data: function () {
    return {
      menuLinks: [
        {
          text: 'Home',
          ref: '#'
        },
        {
          text: 'Shop',
          text2: 'Shop',
          ref: '#'
        },
        {
          text: 'About',
          text2: 'About',
          ref: '#'
        },
        {
          text: 'Gallery',
          text2: 'Gallery',
          ref: '#'
        },
        {
          text: 'Locations',
          text2: 'Locations',
          ref: '#'
        },
        {
          text: 'Journal',
          text2: 'Journal',
          ref: '#'
        },
        { 
          text: 'Contact',
          text2: 'Contact',          
          ref: '#'
        },
        {
          text: 'My Account',
          text2: 'Orders',
          ref: '#'
        }
      ]
    }
  }
};
</script>

<style lang="scss">
@import './styles/general.scss';

</style>
