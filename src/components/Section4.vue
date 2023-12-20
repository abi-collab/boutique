<template>
  <div class="grid grid-cols-4">
    <div v-for="image in images" :key="image.id" class="image-item overflow-hidden">
      <figure>
         <img :src="image.url" alt="Image" class="image" />
      </figure>
  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        { id: 1, url: '../assets/imgs/1.jpg' },
        { id: 2, url: '../assets/imgs/2.jpg' },
        { id: 3, url: '../assets/imgs/3.jpg' },
        { id: 4, url: '../assets/imgs/4.jpg' },
        { id: 1, url: '../assets/imgs/5.jpg' },
        { id: 2, url: '../assets/imgs/6.jpg' },
        { id: 3, url: '../assets/imgs/7.jpg' },
        { id: 4, url: '../assets/imgs/8.jpg' },
      ],
    };
  },
};
</script>
