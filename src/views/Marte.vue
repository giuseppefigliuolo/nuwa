<template>
  <main>
      <hero-section />
      <Lottie
          class="mt-md-16"
          :options="defaultOptions"
          :height="600"
          :width="600"
          @animCreated="handleAnimation"
        />
      <illustration-section
        :titleIllustration="titleIllustration"
      />
      <paragraph-section 
        :title="title"
        :paragraph="paragraph"
      />
  </main>
</template>

<script>
import HeroSection from '../components/HeroSection.vue'
import IllustrationSection from '../components/IllustrationSection.vue'
import Lottie from 'vue-lottie'
import Marte from '@/assets/details_animation.json'
import ParagraphSection from '../components/ParagraphSection.vue'

export default {
  components: {Lottie,HeroSection,IllustrationSection, ParagraphSection},
  name: 'Marte',
  data() {
    return {
      Marte,
      defaultOptions: { animationData: Marte, loop: false },
      animationSpeed: 1,
      titleIllustration:'Scheda tecnica di un viaggiatore Nüwa',
      title: 'Come agiremo sul nuovo pianeta?',
      paragraph: 'La colonizzazione di Marte è un passaggio fondamentale per l’umanità: anche per questo esiste Space X. Noi di Nüwa vogliamo essere i primi a realizzare questo sogno installando la prima colonia umana della storia su territorio marziano.Il nostro progetto si basa sulla volontà di creare un luogo lontano dalla terra vivibile, cosi facendo l’uomo avrà la possibilità di ampliare i propri orizzonti e normalizzare il turismo spaziale.'
    }
  }
}
</script>
