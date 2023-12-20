<script setup>
import Navigation from './components/Navigation.vue';
import Section1 from './components/Section1.vue';
import Section2 from './components/Section2.vue';
import Section3 from './components/Section3.vue';
import Section4 from './components/Section4.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <div id="Heading">
    <Navigation />
    <Section1 />
  
  </div>
  <Section2 />
  <Section3 />
  <Section4 />
  <Footer />
  
</template>

<style scoped>
#Heading {
  background-color: #f5f5f5;
  background-image: url('src/assets/imgs/0.jpg');
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
