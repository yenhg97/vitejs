<template>
  <div>
    <Header />
    <Photos />
  </div>
</template>

<script>
import Header from '@components/Header.vue';
import Photos from '@components/Photos.vue';

export default {
  components: {
    Header,
    Photos
  }
};
</script>