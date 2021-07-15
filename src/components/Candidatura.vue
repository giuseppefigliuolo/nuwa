<template>
  <section>
    <div class="image">
      <img src="@/assets/img/candidatura.webp" :alt="titleMars" />
    </div>
    <div class="text">
      <h2>{{ title }}</h2>
      <p>{{ text }}</p>
      <NuwaBtn :text="btnText" to="/join" />
    </div>
  </section>
</template>

<script>
import NuwaBtn from './NuwaBtn.vue'
export default {
  components: { NuwaBtn },
  props: ['title', 'text', 'btnText']
}
</script>

<style lang="scss" scoped>
section {
  display: flex;
  .text {
    padding: 0 2em;
    display: flex;
    flex-direction: column;
    justify-content: center;
    h2 {
      margin-bottom: 2em;
      font-size: 2em;
    }
    p {
      font-size: 1em;
      line-height: 2;
    }
  }
}
@media screen and (max-width: 700px) {
  section {
    flex-direction: column;
    .image {
      width: 100%;
      img {
        width: 100%;
        height: auto;
      }
    }
    h2 {
      margin-bottom: 1em;
    }
  }
}
</style>
