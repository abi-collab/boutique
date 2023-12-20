<template>
  <div class="grid grid-cols-3 gap-8 px-8 py-24">
    <div class="grid-item">
      <img :src="BirthdayCake" alt="Image 1">
    </div>
    <div class="grid-item">
      <img :src="WeddingCake" alt="Image 2">
    </div>
    <div class="grid-item border border-red-400" >
      <div class="border">
 <img :src="ChristmasCake" alt="Image 3">
      <div class="text-4xl font-bold border ">Christmas Cake</div>
      </div>
     
    </div>
  </div>
</template>

<script setup>
import BirthdayCake from '../assets/imgs/11.jpg';
import WeddingCake from '../assets/imgs/13.jpg';
import ChristmasCake from '../assets/imgs/12.jpg';
</script>

<style>

/* #christmas {
  background-color: #f5f5f5;
  background-image: url('src/assets/imgs/12.jpg');
  background-repeat: no-repeat;
  background-size: cover;
} */

</style>
