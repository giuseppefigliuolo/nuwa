<template>
  <section>
    <div class="full-screen-view">
      <div class="animation-wrapper">
        <LottieAnim class="animazione" :options="defaultOptions" />
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
.animazione{
  height: 600px;
  width:600px;
}
.animation-wrapper {
  width:50%;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items: center;
  transform: translateX(-50%);
}

@media screen and (max-width: 700px){
  .animation-wrapper {
    width:50%;
  }
}
</style>
