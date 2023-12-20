<template>
  <div class="grid grid-cols-3 gap-8 px-2 lg:px-8 py-6 lg:py-12" id="section2">
    <div class="relative">
      <div class="overflow-hidden hover06">
        <figure>
           <img :src="BirthdayCake" alt="Image 3">
        <div class="text-lg md:text-2xl lg:text-4xl absolute bottom-12 mx-auto w-full text-center text-white p-2 productHeads">Birthday Cake</div>
        </figure>
       
      </div>
    </div>
    <div class="relative">
      <div class="overflow-hidden hover06">
        <figure>
            <img :src="WeddingCake" alt="Image 3">
        <div class="text-lg md:text-2xl lg:text-4xl absolute bottom-12 mx-auto w-full text-center text-white p-2 productHeads">Wedding Cake</div>
        </figure>
      
      </div>
    </div>
    <div class="relative">
      <div class="overflow-hidden hover06">
        <figure>
          <img :src="ChristmasCake" alt="Image 3">
        <div class="text-lg md:text-2xl lg:text-4xl absolute bottom-12 mx-auto w-full text-center text-white p-2 productHeads">Christmas Cake</div>
        </figure>
        
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
