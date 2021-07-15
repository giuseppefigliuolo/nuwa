<template>
  <section>
    <h3>{{ title }}</h3>
    <img :src="require(`@/assets/img/${img}`)" :alt="titleIllustration" />
    <p>{{ paragraph }}</p>
    <NuwaBtn :text="btnText" to="/marte" />
  </section>
</template>

<script>
import NuwaBtn from './NuwaBtn.vue'

export default {
  components: { NuwaBtn },
  props: ['title', 'paragraph', 'btnText', 'img']
}
</script>

<style lang="scss" scoped>
section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 70%;
  margin: 0 auto;
  h3 {
    text-align: center;
    font-size: 2em;
    margin-bottom: 4em;
    text-transform: uppercase;
  }
  p {
    font-size: 1.2em;
    margin-bottom: 3em;
    line-height: 2;
    text-align: left;
  }
  img {
    width: 100%;
    height: auto;
    margin-bottom: 4em;
  }
}

@media screen and (max-width: 700px) {
  section {
    max-height: 100%;
    flex-direction: column;
    width: 100%;
    h3 {
      font-size: 1.3em;
      margin-bottom: 1em;
    }
    p {
      font-size: 1.2em;
      line-height: 1.5;
    }
  }
  .left-side {
    width: 100%;
    padding: 2em;
  }
  .image-container {
    width: 100%;

    img {
      width: 100%;
      height: auto;
    }
  }
}
</style>
