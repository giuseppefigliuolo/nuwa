<template>
  <section class="mb-12">
    <v-img
      max-height="800"
      max-width="100%"
      src="@/assets/img/mars-hero.jpeg"
      gradient="to top right, rgba(100,115,201,.23), rgba(25,32,72,.6)"
    />
    <h2 class="hero-title h-font">{{ title }}</h2>
  </section>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Default title'
    }
  }
}
</script>

<style lang="scss" scoped>
section {
  position: relative;
}

.hero-title {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 2.4rem;
}
</style>
