<template>
  <section>
      <div class="text">
          <h2>{{titleMars}}</h2>
          <p>{{textMars}}</p>
      </div>
      <div class="image">
          <img src="@/assets/img/mars-image.jpg" :alt='titleMars'>
      </div>
  </section>
</template>

<script>
export default {
    props: ['titleMars', 'textMars']
}
</script>

<style lang="scss" scoped>
    section{
        margin: 2em 0;
        display: flex;
        justify-content: space-between;
        .image{
            width: 60%;
        }
        .text{
            padding: 0 7em;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            h2{
                font-size: 2.5em;
            }
            p{
                line-height: 2;
                font-size: 1.2em;
            }
        }
    }
</style>