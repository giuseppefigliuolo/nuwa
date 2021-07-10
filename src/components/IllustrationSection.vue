<template>
  <section>
    <div class="title">
      <h3>{{ titleIllustration }}</h3>
    </div>
    <div class="illustration">
      <img
        :src="require('../assets/img/capsule-illustration.png')"
        :alt="title"
      />
    </div>
  </section>
</template>

<script>
export default {
  props: ['titleIllustration']
}
</script>

<style lang="scss" scoped>
section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.title {
  margin: 2em;
  h3 {
    font-size: 2em;
    text-transform: uppercase;
  }
  img {
    width: 100%;
  }
}
@media screen and (max-width: 700px) {
  img {
    width: 100%;
    height: auto;
  }
  .title {
    margin: 1em;
    h3 {
      font-size: 1.3em;
    }
  }
}
</style>
