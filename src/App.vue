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
      books: [
        {
          title: 'Odyssee einer tapferen Frau',
          category: 'Zeitgeschichte',
          description: 'Verena, geboren noch zu Kaisers Zeiten, wuchs frühzeitig als '
          + 'Vollwaise in herrschaftlicher Umgebung auf. Der erste wie zweite Weltkrieg und'
          + ' die hiermit verbundenen Erlebnisse veränderten ihr Leben und das ihrer Kinder.'
          + '\nDer Roman ist nicht frei erfunden, sondern basiert auf tatsächlichen '
          + 'Erlebnissen, zumeist aus dem Verwandten- und Bekanntenkreis des Autors. Sie '
          + 'spiegeln sich in Verena mit all ihren Freuden, Überlebenskämpfen, Sehnsüchten '
          + 'und Erfolgen.',
          bookmundoUrl: '#',
          amazonUrl: '#',
        },
        {
          title: 'Jenseits der goldenen Wiege',
          category: 'Autobiographie',
          description: 'Als Kind mit strengen Schlossmanieren aufgewachsen. Nach dem '
          + 'zweiten Weltkrieg aus der Heimat vertrieben, in einem spartanischen Internat'
          + ' ‚zwischengelagert‘. Mit den Eltern nach Südamerika emigriert und ausgerissen'
          + ' als Jugendlicher in den chilenischen Urwald. Schließlich als Ehemann und Vater'
          + ' auf Mallorca gelandet, im Massentourismus seine Ehe riskierend, um die Existenz'
          + ' gekämpft.',
          bookmundoUrl: '#',
          amazonUrl: '#',
        },
        {
          title: 'Das unsichtbare Paradies',
          category: 'Beziehungsdrama',
          description: 'Ein durchtriebenes Mädchen fängt einen Studenten ein. Er schafft es in'
          + ' die Chefetage und wird mit einem heiklen Auftrag nach Brasilien geschickt. Wegen'
          + ' dieser Frau muss er mit seiner Familie überstürzt das Land verlassen. Er taucht '
          + 'unter und hofft seinen Seelenfrieden in Oberbayern zu finden. ',
          bookmundoUrl: '#',
          amazonUrl: '#',
        },
        {
          title: 'Begegnung in der Sierra Nevada',
          category: 'Dramatischer Liebesroman',
          description: 'Eine sympathische Spanierin ist als Unternehmerin in Hamburg tätig. Zwei'
          + ' traumhafte Männer und ein liebenswertes Mädchen, die eine neue Mutter sucht, sind '
          + 'ihr Problem.',
          bookmundoUrl: '#',
          amazonUrl: '#',
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
