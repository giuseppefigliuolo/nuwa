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
        margin: 2em;
        display: flex;
        justify-content: space-between;
        .image{
            width: 40%;
        }
        .text{
            padding: 0 5em;
            text-align: justify;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            h2{
                font-size: 2em;
                margin-bottom: 1em;
            }
            p{
                line-height: 2;
                font-size: 1em;
            }
        }
    }
    @media screen and (max-width: 700px){
        section{
            margin: 0;
            flex-direction: column;
            .image{
                width: 100%;
                img{
                    width: 100%;
                    height: auto;
                }
            }
            .text{
                padding: 2em;
            }
        }
    }
</style>