<template>
  <div class="bg-black text-white py-48 px-36 h-1/2">
<div class="grid grid-cols-4">
  <div class="col-span-2">


    <form class="max-w-md mx-auto" autocomplete=off>
  <div class="relative z-0 w-full mb-5 group">
      <input  autocomplete="off" type="email" name="floating_email" id="floating_email" class="block py-2.5 px-0 w-full text-sm text-white bg-transparent border-0 border-b-2 border-white appearance-none dark:text-white dark:border-white dark:focus:border-white focus:outline-none focus:ring-0 focus:border-white peer" placeholder=" " required />
      <label for="floating_email" class="peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto peer-focus:text-white peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Email address</label>
  </div>
 <div class="relative z-0 w-full mb-5 group">
        <input autocomplete="off"  type="text" name="floating_first_name" id="floating_first_name" class="block py-2.5 px-0 w-full text-sm text-white bg-transparent border-0 border-b-2 border-white appearance-none dark:text-white dark:border-white dark:focus:border-white focus:outline-none focus:ring-0 focus:border-white peer" placeholder=" " required />
        <label for="floating_first_name" class="peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-white peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">First name</label>
    </div>
    <div class="relative z-0 w-full mb-5 group">
        <input autocomplete="off"  type="text" name="floating_last_name" id="floating_last_name" class="block py-2.5 px-0 w-full text-sm text-white bg-transparent border-0 border-b-2 border-white appearance-none dark:text-white dark:border-white dark:focus:border-white focus:outline-none focus:ring-0 focus:border-white peer" placeholder=" " required />
        <label for="floating_last_name" class="peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-white peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Last name</label>
    </div>
 <div class="relative z-0 w-full mb-5 group">
        <input autocomplete="off"  type="tel" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}" name="floating_phone" id="floating_phone" class="block py-2.5 px-0 w-full text-sm text-white bg-transparent border-0 border-b-2 border-white appearance-none dark:text-white dark:border-white dark:focus:border-white focus:outline-none focus:ring-0 focus:border-white peer" placeholder=" " required />
        <label for="floating_phone" class="peer-focus:font-medium absolute text-sm text-white dark:text-white duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 rtl:peer-focus:translate-x-1/4 peer-focus:text-white peer-focus:dark:text-white peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6">Phone Number</label>
    </div>

  <button type="submit" class=" bg-white text-black hover:bg-white focus:ring-4 focus:outline-none focus:ring-white font-medium rounded-full text-sm w-full sm:w-auto px-8 py-2.5 text-center dark:bg-white dark:hover:bg-white dark:focus:ring-white">Subscribe</button>
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
    <li>sdvsdvsd</li>
    <li>sdvsdvsd</li>
</ul>
  </div>

</div>
  </div>
  <div class="bg-black text-center text-white text-sm py-8">&#169;&nbsp;2023&nbsp;The&nbsp;Cake&nbsp;Boutique.&nbsp;All&nbsp;rights&nbsp;reserved.</div>
</template>
<script setup>

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