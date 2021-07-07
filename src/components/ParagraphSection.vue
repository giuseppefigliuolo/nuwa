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
  max-height: 1000px ;
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
    text-align: left;
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
    max-height: 100%;
    width: 100%;
    height: auto;
  }
}
@media screen and (max-width:700px) {
  section{
    max-height: 100%;
    flex-direction:column;
    width: 100%;
    h3{
    font-size: 1.8em;
    margin-bottom: 1em;
    }
    p{
      font-size: 1.2em;
      line-height: 1.5;
    }
  }
  .left-side{
    width: 100%;
    padding: 2em;
  }
  .image-container{
    width: 100%;

    img{
      width: 100%;
      height: auto;
    }
  }
}
</style>
