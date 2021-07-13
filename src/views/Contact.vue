<template>
  <section>
    <h3>Le iscrizioni apriranno tra...</h3>
    <countdown fontSize="2.8rem" />
  </section>
</template>

<script>
import countdown from '../components/Countdown.vue'
import HeroSection from '../components/HeroSection.vue'
export default {
  components: { countdown, HeroSection }
}
</script>

<style lang="scss" scoped>
section {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  h3{
    font-size: 2em;
    padding-bottom: 3em;
    color: #E7393E;
  }
}
</style>
