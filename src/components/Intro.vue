<template>
  <section>
    <div class="full-screen-view">
      <div class="btn-wrapper">
        <nuwa-btn text="enter" @click.native="introClickHandler" />
      </div>
    </div>
  </section>
</template>

<script>
import NuwaBtn from './NuwaBtn.vue'

export default {
  components: { NuwaBtn },
  methods: {
    introClickHandler() {
      console.log('+++')
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
  position: absolute;
  bottom: 20vh;
  left: 50%;
  transform: translateX(-50%);
}
</style>
