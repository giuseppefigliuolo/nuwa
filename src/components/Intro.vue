<template>
  <section>
    <div class="full-screen-view">
      <div class="animation-wrapper">
        <Lottie
          class="mt-md-16"
          :options="defaultOptions"
          :height="600"
          :width="600"
          @animCreated="handleAnimation"
        />
      </div>
      <div class="btn-wrapper">
        <nuwa-btn text="enter" @click.native="introClickHandler" />
      </div>
    </div>
  </section>
</template>

<script>
import NuwaBtn from './NuwaBtn.vue'
import Lottie from 'vue-lottie'
import logoEntry from '@/assets/logoEntry.json'

export default {
  components: { NuwaBtn, Lottie },
  data() {
    return {
      logoEntry,
      defaultOptions: { animationData: logoEntry, loop: false },
      animationSpeed: 1
    }
  },
  mounted() {
    console.log(logoEntry)
  },
  methods: {
    introClickHandler() {
      this.$events.emit('introBtnClicked')
    },
    handleAnimation(anim) {
      this.anim = anim
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
  bottom: 20vh;
  left: 50%;
  transform: translateX(-50%);
}

.animation-wrapper {
  position: fixed;
  left: 50%;
  transform: translateX(-50%);
}
</style>
