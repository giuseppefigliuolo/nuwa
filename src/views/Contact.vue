<template>
  <section>
    <p>Le iscrizioni apriranno tra...</p>
    <countdown fontSize="2.8rem" />
  </section>
</template>

<script>
import countdown from '../components/Countdown.vue'
export default {
  components: { countdown }
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
