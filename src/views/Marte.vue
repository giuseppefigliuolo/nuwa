<template>
  <main>
      <hero-section />
      <illustration-section
        :titleIllustration="titleIllustration"
      />
      
  </main>
</template>

<script>
import HeroSection from '../components/HeroSection.vue'
import IllustrationSection from '../components/IllustrationSection.vue'

export default {
  name: 'Marte',
  data() {
    return {
      titleIllustration:'Scheda tecnica di un viaggiatore Nüwa '
    }
  },
  components: {
    HeroSection,
    IllustrationSection
  }
}
</script>

<style>

</style>