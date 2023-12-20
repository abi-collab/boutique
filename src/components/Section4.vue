<template>
  <div class="grid grid-cols-4">
    <div v-for="image in images" :key="image.id" class="image-item">
      <img :src="image.url" alt="Image" class="image" />
  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        { id: 1, url: 'src/assets/imgs/1.jpg' },
        { id: 2, url: 'src/assets/imgs/2.jpg' },
        { id: 3, url: 'src/assets/imgs/3.jpg' },
        { id: 4, url: 'src/assets/imgs/4.jpg' },
        { id: 1, url: 'src/assets/imgs/5.jpg' },
        { id: 2, url: 'src/assets/imgs/6.jpg' },
        { id: 3, url: 'src/assets/imgs/7.jpg' },
        { id: 4, url: 'src/assets/imgs/8.jpg' },
      ],
    };
  },
};
</script>
