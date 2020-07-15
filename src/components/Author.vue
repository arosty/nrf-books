<template>
  <div class="card-product bottom-two"> <!--:style="{ backgroundImage: 'url(' + backgroundUrl + ')' }">-->
    <img :src="author.image" />
    <div class="card-product-infos">
      <h3>Der Autor</h3>
      <p>{{ author.bio }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Author',
  props: {
    author: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      /* eslint-disable global-require */
      backgroundUrl: require('@/assets/background.jpg'),
      /* eslint-enable global-require */
    };
  },
};
</script>

<style>


.bottom-two {
    margin-bottom: 5vh;
}
</style>
