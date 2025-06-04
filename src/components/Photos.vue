<template>
  <div class="container">
    <h2>Photo Cards:</h2>
    <div class="card-grid">
      <div class="card" v-for="(card, index) in cards" :key="index">
        <img :src="card.image" :alt="card.title" />
        <div class="title">{{ card.title }}</div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const cards = ref(
  Array.from({ length: 20 }, (_, i) => ({
    image: i % 2 === 0
      ? 'https://i.imgur.com/unmma82.jpeg'
      : 'https://i.imgur.com/2MM9Jqo.jpg',
    title: 'Product name is quite long in some cases'
  }))
);
</script>