<template>
  <main>
    <template v-if="isIntro">
      <intro />
    </template>
    <template v-else>
      <hero-section />
      <illustration-section
        :titleIllustration="titleIllustration"
      />
      <video-section
        :titleVideo="titleVideo" 
      />
      <paragraph-section
        :title="title"
        :paragraph="paragraph"
        :btnText="btnText"
      />
    </template>
  </main>
</template>

<script>
import ParagraphSection from '../components/ParagraphSection.vue'
import Intro from '../components/Intro.vue'
import HeroSection from '../components/HeroSection.vue'
import IllustrationSection from '../components/IllustrationSection.vue'
import VideoSection from '../components/VideoSection.vue'

export default {
  components: { VideoSection },
  name: 'Home',
  data() {
    return {
      title: 'Crea la tua capsula con Nüwa',
      paragraph:
        'Partecipando al progetto interspaziale Nüwa potrai non solo vivere un’esperienza unica ed entrare a far parte della storia dell’umanità. La tua capsula ti accompagnerà per i 9 mesi di viaggio che ti separano da Marte e per questo il nostro obiettivo sarà quello di rendere la tua permanenza nello spazio il più’ confortevole possibile. Per questo motivo Nüwa ti darà la possibilità di creare la tua casa nello spazio, il più’ fedele possibile a quello che desideri. La capsula non si limiterà ad accompagnarti nel viaggio ma diventerà la tua casa per i primi mesi sul nuovo pianeta e per questo al suo interno potrai modificare colori, contenuti, design di pezzi superflui che serviranno solo ed esclusivamente a rendere più confortevole il tuo viaggio. Per vedere tutte le decisioni che puoi prendere vedi la scheda tecnica della capsula e inizia a sognare con Nüwa.',
      btnText: 'ALLA SCOPERTA DI UN NUOVO MONDO',
      isIntro: true,
      titleIllustration:'come sarà la vostra casa ',
      titleVideo:'La tua casa a 60 milioni di km dalla Terra'
    }
  },
  components: {
    ParagraphSection,
    Intro,
    HeroSection,
    IllustrationSection, VideoSection
  },
  mounted() {
    this.$events.on('introBtnClicked', () => {
      this.isIntro = false
    })
  }
}
</script>
