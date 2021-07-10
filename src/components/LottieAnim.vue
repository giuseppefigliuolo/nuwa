<template>
  <Lottie
    class="mt-md-16"
    :options="options"
    :height="height"
    :width="width"
    @animCreated="handleAnimation"
  />
</template>

<script>
import Lottie from 'vue-lottie'

export default {
  components: { Lottie },
  props: {
    height: { type: Number },
    width: { type: Number },
    options: { type: Object, required: true }
  },
  methods: {
    handleAnimation(anim) {
      this.anim = anim
    }
  }
}
</script>

<style lang="scss" scoped></style>
