<template>
  <section>
      <div class="image">
          <img src="@/assets/img/candidatura.webp" alt="">
      </div>
      <div class="context">
          <h2>{{title}}</h2>
          <p>{{text}}</p>
           <NuwaBtn :text="btnText" />
      </div>
  </section>
</template>

<script>
import NuwaBtn from './NuwaBtn.vue'
export default {
    components: {NuwaBtn},
    props: ['title', 'text', 'btnText']
}
</script>

<style lang="scss" scoped>
    section{
        margin-bottom: 2em;
        display: flex;
        .context{
            width: 70%;
            padding: 3em;
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