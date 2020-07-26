<template>
  <div id="app" class="container">
    <!-- <Navbar :author="author"/> -->
    <Header :author="author"/>
    <Author :author="author"/>
    <hr />
    <div v-for="book in books" :key="book.name">
      <Book :book="book"/>
    </div>
    <Impressum/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Header from './components/Header.vue';
import Author from './components/Author.vue';
import Book from './components/Book.vue';
import Impressum from './components/Impressum.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Header,
    Author,
    Book,
    Impressum,
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
      books: [
        {
          title: 'Odyssee einer tapferen Frau',
          category: 'Zeitgeschichte',
          image: require('@/assets/odyssee.jpg'),
          description: 'Verena, geboren noch zu Kaisers Zeiten, wuchs frühzeitig als '
          + 'Vollwaise in herrschaftlicher Umgebung auf. Der erste wie zweite Weltkrieg und'
          + ' die hiermit verbundenen Erlebnisse veränderten ihr Leben und das ihrer Kinder.'
          + '\nDer Roman ist nicht frei erfunden, sondern basiert auf tatsächlichen '
          + 'Erlebnissen, zumeist aus dem Verwandten- und Bekanntenkreis des Autors. Sie '
          + 'spiegeln sich in Verena mit all ihren Freuden, Überlebenskämpfen, Sehnsüchten '
          + 'und Erfolgen.',
          bookmundoUrl: 'https://publish.bookmundo.de/shop/index.php/catalog/product/view/id/509922/s/odysee-einer-tapferen-frau-177010-publish-bookmundo-de/',
          amazonUrl: 'https://www.amazon.de/ODYSEE-EINER-TAPFEREN-Nicolas-Rosty-Forg%C3%A1ch/dp/9463867244/ref=sr_1_3?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=Nicolas+Graf+von+Rosty-Forg%C3%A1ch&qid=1595774323&sr=8-3',
        },
        {
          title: 'Jenseits der goldenen Wiege',
          category: 'Autobiographie',
          image: require('@/assets/wiege.jpg'),
          description: 'Als Kind mit strengen Schlossmanieren aufgewachsen. Nach dem '
          + 'zweiten Weltkrieg aus der Heimat vertrieben, in einem spartanischen Internat'
          + ' ‚zwischengelagert‘. Mit den Eltern nach Südamerika emigriert und ausgerissen'
          + ' als Jugendlicher in den chilenischen Urwald. Schließlich als Ehemann und Vater'
          + ' auf Mallorca gelandet, im Massentourismus seine Ehe riskierend, um die Existenz'
          + ' gekämpft.',
          bookmundoUrl: 'https://publish.bookmundo.de/shop/index.php/jenseits-der-goldenen-wiege-122471-publish-bookmundo-de.html',
          amazonUrl: 'https://www.amazon.de/JENSEITS-GOLDENEN-WIEGE-Nicolas-Rosty-Forg%C3%A1ch/dp/9463423532/ref=sr_1_1?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=Nicolas+Graf+von+Rosty-Forg%C3%A1ch&qid=1595774323&sr=8-1',
        },
        {
          title: 'Das unsichtbare Paradies',
          category: 'Beziehungsdrama',
          image: require('@/assets/paradies.jpg'),
          description: 'Ein durchtriebenes Mädchen fängt einen Studenten ein. Er schafft es in'
          + ' die Chefetage und wird mit einem heiklen Auftrag nach Brasilien geschickt. Wegen'
          + ' dieser Frau muss er mit seiner Familie überstürzt das Land verlassen. Er taucht '
          + 'unter und hofft seinen Seelenfrieden in Oberbayern zu finden. ',
          bookmundoUrl: 'https://publish.bookmundo.de/shop/index.php/catalog/product/view/id/423548/s/das-unsichtbare-paradies-roman-176272-publish-bookmundo-de/',
          amazonUrl: 'https://www.amazon.de/UNSICHTBARE-PARADIES-Nicolas-Graf-Rosty-Forg%C3%A1ch/dp/9463867228/ref=sr_1_4?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=Nicolas+Graf+von+Rosty-Forg%C3%A1ch&qid=1595774323&sr=8-4',
        },
        {
          title: 'Begegnung in der Sierra Nevada',
          category: 'Dramatischer Liebesroman',
          image: require('@/assets/begegnung.jpg'),
          description: 'Eine sympathische Spanierin ist als Unternehmerin in Hamburg tätig. Zwei'
          + ' traumhafte Männer und ein liebenswertes Mädchen, die eine neue Mutter sucht, sind '
          + 'ihr Problem.',
          bookmundoUrl: 'https://publish.bookmundo.de/shop/index.php/begegnung-in-der-sierra-nevada-123089-publish-bookmundo-de.html',
          amazonUrl: 'https://www.amazon.de/BEGEGNUNG-SIERRA-NEVADA-Nicolas-Rosty-Forg%C3%A1ch-ebook/dp/B073QCN4K8/ref=sr_1_2?__mk_de_DE=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=Nicolas+Graf+von+Rosty-Forg%C3%A1ch&qid=1595774323&sr=8-2',
        },
      ],
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
h4 {
  font-size: 17px;
  color: grey;
}
h4 > a {
  font-size: 14px;
}
#app {
  /* background-image: url("./assets/background.jpg"); */
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  /* margin-top: 60px; */
  background-color: '#f1f1f1';
}
#unicorn {
  width: 150px;
  height: auto;
}
</style>
