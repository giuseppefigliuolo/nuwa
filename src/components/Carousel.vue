<template>
  <section>
    <div class="tab fixed-tab vertical-text">
      <div class="border border--gray"></div>
      <div class="content">
        <h2 class="text-uppercase">personale richiesto</h2>
        <p class="text-uppercase">fasi di colonizzazione</p>
      </div>
    </div>
    <v-carousel v-model="model">
      <v-carousel-item v-for="(text, i) in texts" :key="i + text.img">
        <h2>Fase {{ i + 1 }}</h2>
        <div class="border border--gray"></div>
        <p>{{ text.description }}</p>
        <div class="image-wrapper">
          <img :src="`../assets/${text.img}`" alt="" />
        </div>
        <p>{{ text.title }}</p>
        <p v-for="el in text.array" :key="el">{{ el }}</p>
      </v-carousel-item>
    </v-carousel>
  </section>
</template>

<script>
import 'swiper/swiper.scss'

export default {
  data() {
    return {
      model: 0,
      texts: [
        {
          description: `Una delle prime missioni di colonizzazione su Marte sarà quella di trasportare le attrezzature per costruire una "stazione di rifornimento" sul pianeta, e l'astronave stessa sarà il primo insediamento.`,
          img: `step-one`,
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
          img: `step-two`,
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
          img: `step-three`,
          title: 'Chi parteciperà',
          list: ['pilota', 'medici', 'infermieri', 'architetti', 'biologi'],
          color: '#F49911'
        },
        {
          description: `Nell’ultima fase termineremo la colonizzazione con l’arrivo di agricoltori che si occuperanno di “coltivare vegetazioni” che serviranno all’uomo per sopravvivere sul nuovo pianeta.`,
          img: `step-four`,
          title: 'chi parteciperà',
          list: ['pilota', 'medici', 'infermieri', 'agricoltori', 'allevatori'],
          color: '#B82C35'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
section {
  height: 800px;
  margin-bottom: 6rem;
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
