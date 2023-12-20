<template>
  <div class="bg-black text-white py-48 px-36 h-1/2">
<div class="grid grid-cols-4">
  <div class="col-span-2">
    <form class="max-w-md mx-auto" autocomplete=off>
  <div class="relative z-0 w-full mb-5 group">
      <input  autocomplete="off" type="email" name="floating_email" id="floating_email" class="block py-2.5 px-0 w-full text-sm text-white bg-transparent border-0 border-b border-gray-500 appearance-none dark:text-white dark:border-white dark:focus:border-white focus:outline-none focus:ring-0 focus:border-white peer" placeholder=" " required />
      <label for="floating_email" class="peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:text-white peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Email address</label>
  </div>
 <div class="relative z-0 w-full mb-5 group">
        <input autocomplete="off"  type="text" name="floating_first_name" id="floating_first_name" class="block py-2.5 px-0 w-full text-sm text-white bg-transparent border-0 border-b border-gray-500 appearance-none dark:text-white dark:border-white dark:focus:border-white focus:outline-none focus:ring-0 focus:border-white peer" placeholder=" " required />
        <label for="floating_first_name" class="peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-white peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">First name</label>
    </div>
    <div class="relative z-0 w-full mb-5 group">
        <input autocomplete="off"  type="text" name="floating_last_name" id="floating_last_name" class="block py-2.5 px-0 w-full text-sm text-white bg-transparent border-0 border-b border-gray-500 appearance-none dark:text-white dark:border-white dark:focus:border-white focus:outline-none focus:ring-0 focus:border-white peer" placeholder=" " required />
        <label for="floating_last_name" class="peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-white peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Last name</label>
    </div>
 <div class="relative z-0 w-full mb-5 group">
        <input autocomplete="off"  type="tel" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}" name="floating_phone" id="floating_phone" class="block py-2.5 px-0 w-full text-sm text-white bg-transparent border-0 border-b border-gray-500 appearance-none dark:text-white dark:border-white dark:focus:border-white focus:outline-none focus:ring-0 focus:border-white peer" placeholder=" " required />
        <label for="floating_phone" class="peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-white peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Phone Number</label>
    </div>

  <button type="submit" class="py-1.5 tracking-wider rounded-full font-bold text-black bg-white px-6 bg-opacity-80 hover:bg-opacity-90 active:text-black active:bg-white">Subscribe</button>
</form>
  </div>
  <div>
<ul class="grid h-full">
  <li v-for="link in links" :key="link.name">
    <a :href="link.url">{{ link.name }}</a>
    </li>
</ul>
  </div>
  <div>
    <ul class="grid h-full">
  <li v-for="link in notProductLinks" :key="link.name">
    <a :href="link.url">{{ link.name }}</a>
    </li>
    <li>
      <div class="flex justify-start gap-6">
        <a href="#">
          <img :src="tiktok" alt="tiktok" class="h-[30px] bg-white p-1 rounded-full"/>
        </a>
        <a href="#">
          <img :src="youtube" alt="youtube" class="h-[30px] bg-white p-1 rounded-full"/>
        </a>
        <a href="#">
          <img :src="facebook" alt="facebook" class="h-[30px] bg-white p-1 rounded-full"/>
        </a>
        <a href="#">
          <img :src="instagram" alt="instagram" class="h-[30px] bg-white p-1 rounded-full"/>
        </a>
      </div>
    </li>
    <li class="grid place-items-start">
        <div class="bg-white px-8 py-1.5 flex justify-center gap-4 rounded-full">
          <a href="#">
            <img :src="visa" alt="visa" class="h-[50px]"/>
          </a>
          <a href="#">
            <img :src="mastercard" alt="mastercard" class="h-[50px]"/>
          </a>
          <a href="#">
            <img :src="americanExpress" alt="americanExpress" class="h-[50px]"/>
          </a>
          <a href="#">
            <img :src="paypal" alt="paypal" class="h-[50px]"/>
          </a>
      </div>
    </li>
</ul>
  </div>

</div>
  </div>
  <div class="bg-black text-center text-white text-sm py-8">&#169;&nbsp;2023&nbsp;The&nbsp;Cake&nbsp;Boutique.&nbsp;All&nbsp;rights&nbsp;reserved.</div>
</template>
<script setup>
import tiktok from '../assets/tik-tok.svg';
import youtube from '../assets/youtube.svg';
import facebook from '../assets/facebook.svg';
import instagram from '../assets/instagram.svg';

import visa from '../assets/visa.svg';
import mastercard from '../assets/mastercard.svg';
import paypal from '../assets/paypal.svg';
import americanExpress from '../assets/americanExp.svg';

const links = [
  {
    name: 'Signature Cakes',
    url: '#',
  },
  {
    name: 'Bespoke Cakes',
    url: '#',
  },
  {
    name: 'Wedding Cakes',
    url: '#',
  },
  {
    name: 'Cakesicles',
    url: '#',
  },
  {
    name: 'Chocolates',
    url: '#',
  },
  {
    name: 'Master Classes',
    url: '#',
  }];

  const notProductLinks = [
    {
      name: 'Payment And Delivery',
      url: '#',
    },
     {
      name: 'Help Center',
      url: '#',
    },
     {
      name: 'FAQs',
      url: '#',
    },
    {
      name: 'Contact Us',
      url: '#',
    }
  ];



</script>