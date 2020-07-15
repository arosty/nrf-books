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
.card-product {
  overflow: hidden;
  height: 140px;
  background: white;
  /* background-image: './assets/background.jpg'; */
  box-shadow: 0 0 1px rgba(0,0,0,0.1);
  /* width: 100%; */
  display: flex;
  align-items: center;
  transition: 0.3s;
}

.card-product img {
  height: 100%;
  width: 170px;
  object-fit: cover;
  border-radius: 1px;
  /* -webkit-transform: scale(1);
	transform: scale(1);
	-webkit-transition: .3s ease-in-out;
	transition: .3s ease-in-out;
  overflow: hidden;
  flex-shrink: 0; */
}

/* .card-product:hover img {
  -webkit-transform: scale(1.2);
	transform: scale(1.2);
} */

.card-product p {
  font-size: 14px;
  line-height: 1.4;
  opacity: .7;
  margin-bottom: 0;
  margin-top: 8px;
}

.card-product:hover {
  box-shadow: 0 0 3px rgba(0,0,0,0.1);
}

.card-product .card-product-infos {
  padding: 16px;
}

.bottom-two {
    margin-bottom: 5vh;
}
</style>
