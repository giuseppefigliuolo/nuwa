<template>
  <main>
    <template v-if="isIntro">
      <intro />
    </template>
    <template v-else>
      <hero-section title="Le capsule Nuwa nel dettaglio"/>
      <illustration-section
        :titleIllustration="titleIllustration"
        img="capsule-illustration.png"
      />
      <video-section :titleVideo="titleVideo" />
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

export default {
  components: { VideoSection },
  name: 'Home',
  data() {
    return {
      title: 'Crea la tua capsula con Nüwa',
      paragraph:
        'Partecipa al progetto interspaziale Nüwa per un’esperienza unica ed entra a far parte della storia dell’umanità. La capsula costruita per te renderà confortevoli i 9 mesi di viaggio. Nüwa ti darà la possibilità di creare la tua casa nello spazio, il più’ fedele possibile a quello che desideri. Sarà la tua compagna di viaggio e diventerà la tua abitazione per i primi mesi sul nuovo pianeta: potrai scegliere i colori, i contenuti e il design. Guarda la scheda tecnica della capsula e inizia a sognare con Nüwa.',
      btnText: 'SCOPRI IL TUO NUOVO MONDO',
      isIntro: true,
      titleIllustration: 'come sarà la tua casa ',
      titleVideo: 'A 60 milioni di km dalla Terra'
    }
  },
  components: {
    ParagraphSection,
    Intro,
    HeroSection,
    IllustrationSection,
    VideoSection
  },
  mounted() {
    this.$events.on('introBtnClicked', () => {
      this.isIntro = false
    })
  }
}
</script>
