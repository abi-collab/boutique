<template>
  <nav class="w-full">
    <div class="py-14 px-24 flex justify-between">
      <div class="p-2">
        <img :src="boutiqueLogo" alt="boutique-logo" class="h-[72px]" />
      </div>
      <div class="grid place-items-center">
        <ul class="flex gap-12">
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">SIGNATURE CAKES</a></li>
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">BESPOKE CAKES</a></li>
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">WEDDING CAKES</a></li>
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">CAKESICLES</a></li>
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">CHOCOLATES </a></li>
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">MASTER CLASSES</a></li>
        </ul>
      </div>
      <div class="grid place-content-center" >
        <div class="flex justify-center gap-8">
          <img :src="searchIcon" alt="search-icon" class="h-8 text-white" style="filter: invert(100%)" />
          <img :src="userIcon" alt="user-icon" class="h-8 text-white" style="filter: invert(100%)" />
          <img :src="cartIcon" alt="cart-icon" class="h-8 text-white" style="filter: invert(100%)" />
        </div>
      </div>
    </div>

  </nav>
</template>

<script setup>
import boutiqueLogo from '../assets/logo.svg';
import searchIcon from '../assets/search.svg';
import cartIcon from '../assets/shopping-cart.svg';
import userIcon from '../assets/user.svg';

</script>

<style scoped>
nav {
  display: inline-block;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

li {
  display: inline;
  /* margin-right: 10px; */
  color: white;
}

a {
  text-decoration: none;
  color: white;
}
</style>
