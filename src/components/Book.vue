<template>
  <div class="card-product bottom-two"> <!--:style="{ backgroundImage: 'url(' + backgroundUrl + ')' }">-->
    <img :src="book.image" class="product-image" />
    <div class="card-product-infos">
      <h3>{{ book.title }}</h3>
      <h4>{{ book.category }} <a :href="book.bookmundoUrl">Jetzt bestellen</a></h4>
      <p>{{ book.description }}</p>
    </div>
    <div class="buy-icons">
      <a :href="book.bookmundoUrl"><img :src="bookmundoImage" class="buy-icon" /></a>
      <a :href="book.amazonUrl"><img :src="amazonImage" class="buy-icon" /></a>
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
  data() {
    return {
      bookmundoImage: require('@/assets/bookmundo.png'),
      amazonImage: require('@/assets/amazon.svg'),
    };
  }
};
</script>

<style>
.card-product {
  overflow: hidden;
  overflow-y: hidden;
  height: 140px;
  background: white;
  /* background-image: './assets/background.jpg'; */
  box-shadow: 0 0 1px rgba(0,0,0,0.1);
  /* width: 100%; */
  display: flex;
  align-items: center;
  transition: 0.3s;
  position: relative;
}

.buy-icons {
  display: flex;
  align-items: center;
  justify-content: right;
  position: absolute;
  top: 16px;
  right: 16px;
}

.buy-icon {
  height: 18px !important;
  margin-left: 10px;
  overflow: hidden;
  -webkit-transform: scale(1);
	transform: scale(1);
	-webkit-transition: .3s ease-in-out;
	transition: .3s ease-in-out;
  z-index: 2;
}

.buy-icon:hover {
  -webkit-transform: scale(1.2);
	transform: scale(1.2);
}

.card-product img {
  height: 100%;
  width: auto;
  object-fit: cover;
  border-radius: 1px;
  -webkit-transform: scale(1);
	transform: scale(1);
	-webkit-transition: .3s ease-in-out;
	transition: .5s ease-in-out;
  overflow: hidden;
  flex-shrink: 0;
}

/* .card-product:hover .product-image {
  -webkit-transform: scale(1.2);
	transform: scale(1.2);
} */


/*.card-product */
p {
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
  background: white;
  z-index: 1;
  height: 140px;
}

.card-product-infos {
  overflow-y: scroll;
}

 /* Hide scrollbar for Chrome, Safari and Opera */
.card-product-infos::-webkit-scrollbar {
  display: none;
}

/* Hide scrollbar for IE, Edge and Firefox */
.card-product-infos {
  -ms-overflow-style: none;  /* IE and Edge */
  scrollbar-width: none;  /* Firefox */
} 
</style>
