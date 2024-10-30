<script setup>
import Navbar from './components/Navbar.vue';
import Banner from './components/Banner.vue';
import WhyAI from './components/WhyAI.vue';
import WhyUs from './components/WhyUs.vue';
import Partners from './components/Partners.vue';
</script>

<template>

  <Navbar />
  <Banner />
  <WhyAI />
  <WhyUs />
  <Partners />

</template>

<style scoped>
/* @media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
} */
</style>
