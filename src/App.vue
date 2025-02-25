<template>
  <div id="app">
    <Hero />
    <InfoOne />
    <Slider />


    <Blog />
    <FAQ />
    <Footer />
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Slider from "./components/Slider.vue";
import InfoOne from "./components/InfoOne.vue";
import Blog from "./components/Blog.vue";
import FAQ from "./components/FAQ.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Hero,
    InfoOne,
    Slider,
    Blog,
    FAQ,
    Footer,
  },
};
</script>

<style>
html, body {
  margin: 0;
  padding: 0;
  box-sizing: border-box; 
  background-color: #F3F3F3;
  user-select: none;
  /* width: 100vw; */
  overflow-x: hidden;
}
</style>