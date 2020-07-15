<template>
  <div id="app" class="container">
    <Navbar :author="author"/>
    <Header :author="author"/>
    <Author :author="author"/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Header from './components/Header.vue';
import Author from './components/Author.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Header,
    Author,
  },
  data() {
    return {
      author: {
        name: 'Nicolas Graf von Rosty-Forgách',
        /* eslint-disable global-require */
        image: require('@/assets/nrf_portrait.jpg'),
        /* eslint-enable global-require */
        bio: 'Nicolas ist als ungarischer Diplomatensohn in Prag geboren. Seine Kindheit '
        + 'verbrachte er auf den Schlössern seiner Familie.  Nach dem Krieg wurde die'
        + ' Familie enteignet und wanderte als Flüchtlinge nach Südamerika aus. Der '
        + 'Autor nahm die chilenische Staatbürgerschaft an, heiratete eine Deutsche. '
        + 'Mit zwei Kindern kehrt die junge Familie nach Europa zurück. Er lebt nun '
        + 'mit seiner Frau in Lenggries, Bayern.',
      },
    };
  },
};
</script>

<style>
/* @import './assets/styles.css'; */
h1 {
  font-family: 'Aguafina Script';
  font-size: 50px;
  text-align: center;
}
h2 {
  font-size: 30px;
}
h3 {
  font-size: 20px;
}
#app {
  /* background-image: url("./assets/background.jpg"); */
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  /* margin-top: 60px; */
}
#unicorn {
  width: 150px;
  height: auto;
}
</style>
