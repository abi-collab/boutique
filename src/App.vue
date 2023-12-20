<script setup>
import Navigation from './components/Navigation.vue';
import Section1 from './components/Section1.vue';
import Section2 from './components/Section2.vue';
import Section3 from './components/Section3.vue';
import Section4 from './components/Section4.vue';
import Footer from './components/Footer.vue';
import image0 from './assets/imgs/0.jpg';
</script>

<template>
  <div id="Heading" :style="{backgroundImage: 'url(' + image0 + ')', backgroundRepeat: 'no-repeat', backgroundSize: 'cover'}">
    <Navigation />
    <Section1 />
  
  </div>
  <Section2 />
  <Section3 />
  <Section4 />
  <Footer />
  
</template>

<!-- <style scoped>
#Heading {
  background-image: url(image0);
  
}
</style> -->
