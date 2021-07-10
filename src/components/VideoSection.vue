<template>
  <section>
    <h3>{{ titleVideo }}</h3>
    <LottieAnim :width="600" :height="600" :options="options" />
  </section>
</template>

<script>
import LottieAnim from './LottieAnim.vue'
import homeAnimation from '@/assets/lottie/homeAnimation.json'

export default {
  components: { LottieAnim },
  props: ['titleVideo'],
  data() {
    return {
      options: { animationData: homeAnimation, loop: false }
    }
  }
}
</script>

<style lang="scss" scoped>
section {
  margin-top: 3rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  video {
    width: 100%;
  }
  h3 {
    font-size: 2em;
    text-transform: uppercase;
  }
}
@media screen and (max-width: 700px) {
  section {
    padding: 2em;
    margin-top: 2rem;
    h3 {
      font-size: 1.3em;
    }
  }
}
</style>
