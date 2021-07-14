<template>
  <main>
    <template v-if="isIntro">
      <intro />
    </template>
    <template v-else>
      <hero-section 
        title="Scopri le capsule NUWA"
      />
      <illustration-section
        :titleIllustration="titleIllustration"
        img="capsule-illustration.webp"
        :punto1="punto1"
        :punto2="punto2"
        :punto3="punto3"
        :punto4="punto4"
        :punto5="punto5"
      />
      <h2>A 60 milioni di km dalla Terra</h2>
      <video autoplay loop muted width="100%" height="auto">
        <source
          src="../assets/lottie/marte-animation.webm"
          type="video/webm"
        />
        Sorry, your browser doesn't support embedded videos.
      </video>
      <paragraph-section
        :title="title"
        :paragraph="paragraph"
        :btnText="btnText"
        img="sezione_capsula.png"
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
        'Partecipa al progetto interspaziale Nüwa per un’esperienza unica ed entra a far parte della storia dell’umanità. La capsula costruita per te renderà confortevoli i 9 mesi di viaggio. Nüwa ti darà la possibilità di creare la tua casa nello spazio, il più’ fedele possibile a quello che desideri. Sarà la tua compagna di viaggio e diventerà la tua abitazione per i primi mesi sul nuovo pianeta: potrai scegliere i colori, i contenuti e il design. Guarda la scheda tecnica della capsula e inizia a sognare con Nüwa.',
      btnText: 'SCOPRI IL TUO NUOVO MONDO',
      isIntro: true,
      titleIllustration: 'come sarà la tua casa ',
      punto1:'Capsule 4x4 attorno alla navicella madre',
      punto2:'Trasporta fino a 150 tonnellate di carico',
      punto3:'Motore RAPTOR VACUM',
      punto4:'Combustibile raffinabile su Marte',
      punto5:'Navicella madre con aree comuni per i viaggiatori',
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
<style leng="scss" scoped>
  h2{
    font-size: 2em;
    text-align: center;
    margin: 2em 0;
    text-transform: uppercase;
  }
  video{
    margin: 8em 0;
  }
  @media screen and (max-width:700px) {
    video{
      margin: 2em 0 ;
    }    
  }
</style>