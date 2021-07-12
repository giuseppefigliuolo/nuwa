<template>
  <main>
    <illustration-section
      :titleIllustration="titleIllustration"
      img="man.png"
    />
    <paragraph-section
      :title="title"
      :paragraph="paragraph"
      img="@/assets/img/capsule-illustration.png"
    />
  </main>
</template>

<script>
import HeroSection from '../components/HeroSection.vue'
import IllustrationSection from '../components/IllustrationSection.vue'
import LottieAnim from '@/components/LottieAnim.vue'
import ParagraphSection from '../components/ParagraphSection.vue'

export default {
  components: {
    LottieAnim,
    HeroSection,
    IllustrationSection,
    ParagraphSection,
    Video
  },
  name: 'Marte',
  data() {
    return {
      Marte,
      titleIllustration: 'Scheda tecnica di un viaggiatore Nüwa',
      title: 'Come agiremo sul nuovo pianeta?',
      paragraph:
        'La colonizzazione di Marte è un passaggio fondamentale per l’umanità: anche per questo esiste Space X. Noi di Nüwa vogliamo essere i primi a realizzare questo sogno installando la prima colonia umana della storia su territorio marziano.Il nostro progetto si basa sulla volontà di creare un luogo lontano dalla terra vivibile, cosi facendo l’uomo avrà la possibilità di ampliare i propri orizzonti e normalizzare il turismo spaziale.'
    }
  }
}
</script>
