<script>
import Pricing from "./Pricing.vue";
import Nav from "./Nav.vue";
import Hero from "./Hero.vue";
import Work from "./Work.vue";
import About from "./About.vue";
import CTA from "./CTA.vue";
import Why from "./Why.vue";
import Footer from "./Footer.vue";
import Tech from "./Tech.vue";

export default {
  components: { Tech, Why, CTA, About, Work, Hero, Nav, Pricing, Footer },
  data() {
    return {
      showMenu: false,
    };
  },
};
</script>

<template>
  <div class="banner-1">
    <Nav />
    <Hero />
  </div>
  <Why />
  <Work />
  <Tech />
  <Pricing />
  <About />
  <CTA />
  <Footer />
</template>
