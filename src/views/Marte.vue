<template>
  <main>
    <!-- <hero-section title="Marte"/> -->
    <div id="app">
      <div class="container">
        <video autoplay muted width="100%">
          <source
            src="../assets/lottie/marte-animation.webm"
            type="video/webm"
          />
          Sorry, your browser doesn't support embedded videos.
        </video>
      </div>
    </div>
    <illustration-section
      :titleIllustration="titleIllustration"
      img="man.webp"
      :punto1="punto1"
      :punto2="punto2"
      :punto3="punto3"
      :punto4="punto4"
      :punto5="punto5"
    />
    <info-marte :titleMars="titleMars" :textMars="textMars" />
    <carousel />
    <candidatura :title="title" :text="text" :btnText="btnText" />
  </main>
</template>

<script>
import HeroSection from '../components/HeroSection.vue'
import IllustrationSection from '../components/IllustrationSection.vue'
import LottieAnim from '@/components/LottieAnim.vue'
import Carousel from '../components/Carousel.vue'
import Candidatura from '../components/Candidatura.vue'
import InfoMarte from '../components/InfoMarte.vue'

export default {
  components: {
    LottieAnim,
    HeroSection,
    IllustrationSection,
    Carousel,
    Candidatura,
    InfoMarte
  },
  name: 'Marte',
  data() {
    return {
      titleIllustration: 'Scheda tecnica di un viaggiatore Nüwa',
      titleMars: 'Come agiremo sul nuovo pianeta?',
      textMars:
        'La colonizzazione di Marte è un passaggio fondamentale per l’umanità: anche per questo esiste Space X. Noi di Nüwa vogliamo essere i primi a realizzare questo sogno installando la prima colonia umana della storia su territorio marziano.Il nostro progetto si basa sulla volontà di creare un luogo lontano dalla terra vivibile, cosi facendo l’uomo avrà la possibilità di ampliare i propri orizzonti e normalizzare il turismo spaziale.',

      title: 'Hai tutti i requisiti che cerchiamo? Vuoi cambiare la tua vita?',
      text:
        'Se pensi di essere la persona che stiamo cercando, mandaci la tua candidatura. Allontanati dalla monotonia della Terra e diventa un vero astronauta, facci vedere di cosa sei capace e porta le tue abilità con noi su Marte.',
      btnText: 'Canditati con Nüwa ',
      punto1: '10/10 di vista (occhiali e lenti si)',
      punto2: 'Nessuna malattia e/o dipendenza',
      punto3: 'Nessun disturbo psicologico',
      punto4: 'Saper nuotare bene',
      punto5: 'Livello alto di allenamento fisico'
    }
  }
}
</script>
