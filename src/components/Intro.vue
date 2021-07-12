<template>
  <section>
    <div class="full-screen-view">
      <div class="animation-wrapper">
        <LottieAnim :width="600" :height="600" :options="defaultOptions" />
      </div>
      <div class="btn-wrapper">
        <nuwa-btn text="enter" @click.native="introClickHandler" />
      </div>
    </div>
  </section>
</template>

<script>
import NuwaBtn from './NuwaBtn.vue'
import logoEntry from '@/assets/lottie/logoEntry.json'
import LottieAnim from '@/components/LottieAnim.vue'

export default {
  components: { NuwaBtn, LottieAnim },
  data() {
    return {
      logoEntry,
      defaultOptions: { animationData: logoEntry, loop: false },
      animationSpeed: 1
    }
  },
  methods: {
    introClickHandler() {
      this.$events.emit('introBtnClicked')
    }
  }
}
</script>

<style lang="scss" scoped>
.full-screen-view {
  width: 100vw;
  height: 100vh;
}

.btn-wrapper {
  position: fixed;
  bottom: 10vh;
  left: 50%;
  transform: translateX(-50%);
}

.animation-wrapper {
  position: fixed;
  left: 50%;
  transform: translateX(-50%);
}
</style>
