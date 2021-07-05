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
  width: 100%;
  h3{
    font-size: 3em;
    margin-bottom: 2em;
  }
  p{
    font-size: 1.2em;
    margin-bottom: 3em;
    line-height: 2;
    text-align: justify;
  }
}
.left-side{
  width: 50%;
  padding: 0 8em;
  display: flex;
  flex-direction: column;
}
.image-container{
  width: 50%;
  img{
    width: 100%;
    height: auto;
  }
}
</style>
