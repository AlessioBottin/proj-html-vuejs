<template>
  <div id="app">
    <Header />

    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui ea delectus ad dolorem repellat dicta perspiciatis molestias earum fugiat nihil quod, doloribus vero, laboriosam maxime veniam accusamus nesciunt omnis! Nihil.</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui ea delectus ad dolorem repellat dicta perspiciatis molestias earum fugiat nihil quod, doloribus vero, laboriosam maxime veniam accusamus nesciunt omnis! Nihil.</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui ea delectus ad dolorem repellat dicta perspiciatis molestias earum fugiat nihil quod, doloribus vero, laboriosam maxime veniam accusamus nesciunt omnis! Nihil.</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui ea delectus ad dolorem repellat dicta perspiciatis molestias earum fugiat nihil quod, doloribus vero, laboriosam maxime veniam accusamus nesciunt omnis! Nihil.</p>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Qui ea delectus ad dolorem repellat dicta perspiciatis molestias earum fugiat nihil quod, doloribus vero, laboriosam maxime veniam accusamus nesciunt omnis! Nihil.</p>
    <FloatingButtons />

    <Main />

    <Footer />
  </div>
</template>

<script>
import "@fontsource/roboto";
import "@fontsource/open-sans";
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
