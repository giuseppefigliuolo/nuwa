<template>
  <section>
    <hero-section title="Le iscrizioni apriranno tra..." />
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
}
</style>
