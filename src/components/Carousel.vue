<template>
  <section>
    <div class="tab fixed-tab vertical-text">
      <div class="border border--gray"></div>
      <div class="content">
        <h2 class="text-uppercase">personale richiesto</h2>
        <p class="text-uppercase">fasi di colonizzazione</p>
      </div>
    </div>
    <v-carousel v-model="model" class="carousel" height="100%">
      <v-carousel-item v-for="(text, i) in texts" :key="i + text.img" dark>
        <h2>Fase {{ i + 1 }}</h2>
        <div class="border" :style="{ 'background-color': text.color }"></div>
        <p>{{ text.description }}</p>
        <v-img :src="text.img" alt="" max-height="400" max-width="500" />
        <p>{{ text.title }}</p>
        <p v-for="el in text.list" :key="el">{{ el }}</p>
      </v-carousel-item>
    </v-carousel>
  </section>
</template>

<script>
import 'swiper/swiper.scss'
import imageOne from '../assets/img/step-one.webp'
import imageTwo from '../assets/img/step-two.webp'
import imageThree from '../assets/img/step-three.webp'
import imageFour from '../assets/img/step-four.webp'

export default {
  data() {
    return {
      model: 0,
      texts: [
        {
          description: `Una delle prime missioni di colonizzazione su Marte sarà quella di trasportare le attrezzature per costruire una "stazione di rifornimento" sul pianeta, e l'astronave stessa sarà il primo insediamento.`,
          img: imageOne,
          title: 'partecipanti alla spedizione',
          list: [
            'pilota',
            'medici',
            'infermieri',
            'ingegneri spaziali',
            'ingegneri di materiali'
          ],
          color: '#B82C35'
        },
        {
          description: `Nella seconda fase ci concentreremo sullo studio dei terreni e della struttura del pianeta in modo fda potre iniziare la “progettazione della prime case e delle prime coltivazioni” su pianeta.`,
          img: imageTwo,
          title: 'partecipanti alla spedizione',
          list: [
            'pilota',
            'medici',
            'infermieri',
            'astrobiologi',
            'architetti spaziali'
          ],
          color: '#70C3BB'
        },
        {
          description: `Nella terza fase procederemo con la “realizzazione di abitazioni e strutture pubbliche” e con lo “studio generico della flora e della fauna” utili allo sviluppo.`,
          img: imageThree,
          title: 'Chi parteciperà',
          list: ['pilota', 'medici', 'infermieri', 'architetti', 'biologi'],
          color: '#F49911'
        },
        {
          description: `Nell’ultima fase termineremo la colonizzazione con l’arrivo di agricoltori che si occuperanno di “coltivare vegetazioni” che serviranno all’uomo per sopravvivere sul nuovo pianeta.`,
          img: imageFour,
          title: 'chi parteciperà',
          list: ['pilota', 'medici', 'infermieri', 'agricoltori', 'allevatori'],
          color: '#B82C35'
        }
      ]
    }
  },
  mounted() {
    console.log()
  }
}
</script>

<style lang="scss" scoped>
section {
  height: 90vh;
  margin-bottom: 6rem;

  display: flex;
}

.carousel {
  > * {
    color: white !important;
  }
}

.tab {
  height: 100%;
  display: flex;
  flex-direction: row-reverse;
}

.vertical-text {
  writing-mode: vertical-rl;
  text-orientation: mixed;
  transform: scale(-1);
}

.fixed-tab {
  width: 110px;

  .content {
    height: 70%;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
}

.border {
  margin-bottom: auto;
  height: 48px;
  width: 100%;
  &--gray {
    background: gray;
  }
}
</style>
