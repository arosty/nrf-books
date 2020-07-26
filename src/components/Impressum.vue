<template>
  <div class="top-four">
    <p @click="showImp = !showImp" class="impressum"><b>IMPRESSUM</b></p>
    <template v-if="showImp">
    <p><b>Verantwortlich für den Inhalt:</b></p>
    <p>Nicolas Graf von Rosty-Forgách<br>Urtlmühlweg 2<br>83661 Lenggries<br>08042 / 9 74 00 22<br>rosty-forgach@t-online.de</p>
    <p><b>Haftung für Links:</b></p>
    <p>Meine Webseite enthält Links zu externen Webseiten Dritter, auf deren Inhalte ich keinen Einfluss habe. Deshalb kann ich für diese fremden Inhalte auch keine Gewähr übernehmen. Für die Inhalte der verlinkten Seiten ist stets der jeweilige Anbieter oder Betreiber der Seiten verantwortlich. Die verlinkten Seiten wurden zum Zeitpunkt der Verlinkung auf mögliche Rechtsverstöße überprüft. Rechtswidrige Inhalte waren zum Zeitpunkt der Verlinkung nicht erkennbar. Eine permanente inhaltliche Kontrolle der verlinkten Seiten ist jedoch ohne konkrete Anhaltspunkte einer Rechtsverletzung nicht zumutbar. Bei Bekanntwerden von Rechtsverletzungen werde ich derartige Links umgehend entfernen.</p>
    <p><b>Urheber- und Kennzeichenrecht</b></p>
    <p>Der Autor ist bestrebt, in allen Publikationen die Urheberrechte der verwendeten Bilder, Grafiken, Tondokumente, Videosequenzen und Texte zu beachten, von ihm selbst erstellte Bilder, Grafiken, Tondokumente, Videosequenzen und Texte zu nutzen oder auf lizenzfreie Grafiken, Tondokumente, Videosequenzen und Texte zurückzugreifen. Alle innerhalb des Internetangebotes genannten und ggf. durch Dritte geschützten Marken- und Warenzeichen unterliegen uneingeschränkt den Bestimmungen des jeweils gültigen Kennzeichenrechts und den Besitzrechten der jeweiligen eingetragenen Eigentümer. Allein aufgrund der bloßen Nennung ist nicht der Schluss zu ziehen, dass Markenzeichen nicht durch Rechte Dritter geschützt sind! Das Copyright für veröffentlichte, vom Autor selbst erstellte Objekte bleibt allein beim Autor der Seiten. Eine Vervielfältigung oder Verwendung solcher Grafiken, Tondokumente, Videosequenzen und Texte in anderen elektronischen oder gedruckten Publikationen ist ohne ausdrückliche Zustimmung des Autors nicht gestattet.</p>
    </template>
  </div>
</template>

<script>
export default {
  name: 'Impressum',
  props: {
    author: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      showImp: false,
      /* eslint-disable global-require */
      backgroundUrl: require('@/assets/background.jpg'),
      /* eslint-enable global-require */
    };
  },
};
</script>

<style>
.impressum:hover {
  cursor: pointer;
}

.top-four {
    margin-top: 8vh;
}
</style>