<template>
<div id="author">
  <div class="card-product bottom-two"> <!--:style="{ backgroundImage: 'url(' + backgroundUrl + ')' }">-->
    <div class="card-product-infos">
      <h3>Der Autor</h3>
      <p>{{ author.bio }}</p>
    </div>
    <img :src="author.image" class="author-image" />
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
.author-image {
  display: block;
  margin: auto;
  width: 20%;
}

#author .card-product {
  /* height: 170px; */
}


.bottom-two {
    margin-bottom: 5vh;
}

</style>
