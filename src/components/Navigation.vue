<template>
  <nav class="w-full bg-black bg-opacity-40">
    <div class="py-4 xs:px-0 md:px-8 grid grid-cols-5">
      <div class="p-2 col-span-5 lg:col-span-1 px-8 md:px-0">
        <img :src="boutiqueLogo" alt="boutique-logo" class="h-[72px]" />
      </div>
    <div class="hidden md:grid place-items-center w-full px-4 md:px-8 lg:px-4 col-span-5 lg:col-span-3 mt-6 md:mt-0">
        <ul class="flex flex-wrap gap-6 transition" v-if="!isSearch">
          <li class="tracking-widest text-xs md:text-lg"><a href="#">SIGNATURE CAKES</a></li>
          <li class="tracking-widest text-xs md:text-lg"><a href="#">BESPOKE CAKES</a></li>
          <li class="tracking-widest text-xs md:text-lg"><a href="#">WEDDING CAKES</a></li>
          <li class="tracking-widest text-xs md:text-lg"><a href="#">CAKESICLES</a></li>
          <li class="tracking-widest text-xs md:text-lg"><a href="#">CHOCOLATES </a></li>
          <li class="tracking-widest text-xs md:text-lg"><a href="#">MASTER CLASSES</a></li>
        </ul>
        <div class="w-full transition opacity-90" ref="target" v-else>
          <input type="text" class="drop-shadow-xl rounded-full px-4 py-2 w-full text-black tracking-wider" placeholder="Search..." v-on:keyup.enter="isSearch = !isSearch" />
        </div>
    </div>
      <div class="md:hidden ml-4 w-full col-span-3 flex">
        <img :src="burgerIcon" alt="burger-icon" class="h-10 md:h-8 text-white hover:cursor-pointer mt-2" style="filter: invert(100%)" @click="isDropdownOpen = !isDropdownOpen" />
        <input type="text" class=" px-2 rounded-full w-full text-black" placeholder="Search..." v-if="isSearch" v-on:keyup.enter="isSearch = !isSearch" />
      </div>
      <div class="grid place-content-start lg:place-content-center col-span-2 lg:col-span-1 mt-6 lg:mt-0 px-8 md:px-0" >
        <div class="flex justify-center gap-8">
          <a href="#" class="inline-block">
            <img :src="searchIcon" alt="search-icon" class="h-6 md:h-8 text-white" style="filter: invert(100%)" @click="isSearch = !isSearch" />
          </a>
          <a href="#" class="inline-block">
            <img :src="userIcon" alt="user-icon" class="h-6 md:h-8 text-white" style="filter: invert(100%)" />
          </a>
          <a href="#" class="inline-block">
            <img :src="cartIcon" alt="cart-icon" class="h-6 md:h-8 text-white" style="filter: invert(100%)" />
          </a>
        </div>
      </div>
    </div>
    <div class="bg-black absolute ml-4 block md:hidden" :class="{ 'hidden': !isDropdownOpen }" style="z-index: 9999;" v-on:keyup.enter="isDropdownOpen = false">
      <h1 class="tracking-widest text-xs md:text-lg block py-4 px-4 text-white hover:text-black hover:bg-white hover:cursor-pointer" @click="isDropdownOpen = !isDropdownOpen">SIGNATURE CAKES</h1>
      <h1 class="tracking-widest text-xs md:text-lg block py-4 px-4 text-white hover:text-black hover:bg-white hover:cursor-pointer" @click="isDropdownOpen = !isDropdownOpen">BESPOKE CAKES</h1>
      <h1 class="tracking-widest text-xs md:text-lg block py-4 px-4 text-white hover:text-black hover:bg-white hover:cursor-pointer" @click="isDropdownOpen = !isDropdownOpen">WEDDING CAKES</h1>
      <h1 class="tracking-widest text-xs md:text-lg block py-4 px-4 text-white hover:text-black hover:bg-white hover:cursor-pointer" @click="isDropdownOpen = !isDropdownOpen">CAKESICLES</h1>
      <h1 class="tracking-widest text-xs md:text-lg block py-4 px-4 text-white hover:text-black hover:bg-white hover:cursor-pointer" @click="isDropdownOpen = !isDropdownOpen">CHOCOLATES</h1>
      <h1 class="tracking-widest text-xs md:text-lg block py-4 px-4 text-white hover:text-black hover:bg-white hover:cursor-pointer" @click="isDropdownOpen = !isDropdownOpen">MASTER CLASSES</h1>
    </div>
  </nav>
</template>

<script setup>
import { ref }  from 'vue';
import boutiqueLogo from '../assets/logo.svg';
import searchIcon from '../assets/search.svg';
import cartIcon from '../assets/shopping-cart.svg';
import userIcon from '../assets/user.svg';
import burgerIcon from '../assets/burger.svg';
import { onClickOutside } from '@vueuse/core'

let isSearch = ref(false);
const target = ref(null);

let isDropdownOpen = ref(false);

onClickOutside(target, event => {
  isSearch.value = false;
  isDropdownOpen.value = false;
})
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
