<template>
  <div class="card-product bottom-two"> <!--:style="{ backgroundImage: 'url(' + backgroundUrl + ')' }">-->
    <img :src="author.image" />
    <div class="card-product-infos">
      <h3>{{ book.title }}</h3>
      <h4>{{ book.category }}</h4>
      <p>{{ book.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Book',
  props: {
    book: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style>
</style>
