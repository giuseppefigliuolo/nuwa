<template>
  <section>
    <div class="left-side">
      <h3>{{ title }}</h3>
      <p>{{ paragraph }}</p>
      <NuwaBtn :text="btnText" />
    </div>
    <div class="image-container">
      <img :src="require('../assets/violet-capsule.jpg')" :alt="title" />
    </div>
  </section>
</template>

<script>
import NuwaBtn from './NuwaBtn.vue'

export default {
  components: { NuwaBtn },
  props: ['title', 'paragraph', 'btnText', 'imgPath']
}
</script>

<style lang="scss" scoped>
section {
  display: flex;
}
</style>
