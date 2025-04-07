<template>
  <div id="app">
    <Hero />
    <TextComponent />
    <!-- tema 1 -->
    <InfoOne />
    <Slider />

    <!-- tema 2 -->
    <InfoTwo />
    <SliderTwo />

    <!-- tema 3 -->
    <InfoThree />
    <SliderThree />

    <Blog />
    <FAQ />
    <Footer />
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import TextComponent from "./components/TextComponent.vue";

/* tema 1 */
import InfoOne from "./components/InfoOne.vue";
import Slider from "./components/Slider.vue";

/* tema 2 */
import InfoTwo from "./components/InfoTwo.vue";
import SliderTwo from "./components/SliderTwo.vue";

/* tema 3 */
import InfoThree from "./components/InfoThree.vue";
import SliderThree from "./components/SliderThree.vue";

import Blog from "./components/Blog.vue";
import FAQ from "./components/FAQ.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Hero,
    TextComponent,
    /* tema 1 */
    InfoOne,
    Slider,

    /* tema 2 */
    InfoTwo,
    SliderTwo,
    
    /* tema 3 */
    InfoThree,
    SliderThree,

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