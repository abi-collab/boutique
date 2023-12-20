<template>
  <nav class="w-full bg-black bg-opacity-40">
    <div class="py-4 px-24 flex justify-between">
      <div class="p-2">
        <img :src="boutiqueLogo" alt="boutique-logo" class="h-[72px]" />
      </div>
      <div class="grid place-items-center w-full px-24">
        <ul class="flex gap-12 transition" v-if="!isSearch">
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">SIGNATURE CAKES</a></li>
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">BESPOKE CAKES</a></li>
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">WEDDING CAKES</a></li>
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">CAKESICLES</a></li>
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">CHOCOLATES </a></li>
          <li class="tracking-widest"><a href="#" class="font-normal drop-shadow-sm">MASTER CLASSES</a></li>
        </ul>
        <div class="w-full transition opacity-90" ref="target" v-else>
          <input type="text" class="drop-shadow-xl rounded-full px-4 py-2 w-full text-black tracking-wider" placeholder="Search..." v-on:keyup.enter="isSearch = !isSearch" />
        </div>
      </div>
      <div class="grid place-content-center" >
        <div class="flex justify-center gap-8">
          <a href="#" class="inline-block">
            <img :src="searchIcon" alt="search-icon" class="h-8 text-white" style="filter: invert(100%)" @click="isSearch = !isSearch" />
          </a>
          <a href="#" class="inline-block">
            <img :src="userIcon" alt="user-icon" class="h-8 text-white" style="filter: invert(100%)" />
          </a>
          <a href="#" class="inline-block">
            <img :src="cartIcon" alt="cart-icon" class="h-8 text-white" style="filter: invert(100%)" />
          </a>
        </div>
      </div>
    </div>

  </nav>
</template>

<script setup>
import { ref }  from 'vue';
import boutiqueLogo from '../assets/logo.svg';
import searchIcon from '../assets/search.svg';
import cartIcon from '../assets/shopping-cart.svg';
import userIcon from '../assets/user.svg';
import { onClickOutside } from '@vueuse/core'

let isSearch = ref(false);
const target = ref(null);

onClickOutside(target, event => isSearch.value = false)
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
