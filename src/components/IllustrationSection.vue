<template>
  <section>
    <div class="title">
      <h3>{{ titleIllustration }}</h3>
    </div>
    <div class="flex">
      <div class="illustration">
        <img :src="require(`@/assets/img/${img}`)" :alt="titleIllustration" />
      </div>
      <div id="wrapper">
        <p class="glitch" :data-text="punto1">{{punto1}}</p>
		    <p class="glitch" :data-text="punto2">{{punto2}}</p>
        <p class="glitch" :data-text="punto3">{{punto3}}</p>
        <p class="glitch" :data-text="punto4">{{punto4}}</p>
        <p class="glitch" :data-text="punto5">{{punto5}}</p>
	    </div>

    </div>

  </section>
</template>

<script>
export default {
  props: ['titleIllustration', 'img', 'punto1', 'punto2', 'punto3', 'punto4', 'punto5']
}
</script>

<style lang="scss" scoped>
section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-bottom: 6rem;
}
.title {
  margin: 2em;
  h3 {
    font-size: 2em;
    text-transform: uppercase;
    margin: 2em 0;
  }
}
.illustration{
  width: 50%;
  display: flex;
  justify-content: center;
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
  .flex{
    flex-direction: column;
  }
  .illustration{
    width: 100%;
  }
  #wrapper{
    width: 100%;
  }
}


.flex{
  display: flex;
  width: 100%;
  margin-bottom: 2em;
}
.illustration{
  width: 50%;
}
// glitch text
  #wrapper {
    text-align: left;
    width: 50%;
    margin: 1em 3em;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .sub {
    color: rgb(100,220,220);
    letter-spacing: 1em;
  }
  @mixin glitchCopy { 
      content: attr(data-text);
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
  }

  .glitch {
    position: relative;
    color: white;
    font-size: 1.5em;
    letter-spacing: .5em;
    animation: glitch-skew 1s infinite linear alternate-reverse;
    &::before{
      @include glitchCopy;
      left: 2px;
      text-shadow: -2px 0 #ff00c1;
      clip: rect(44px, 450px, 56px, 0);
      animation: glitch-anim 5s infinite linear alternate-reverse;
    }
    &::after {
      @include glitchCopy;
      left: -2px;
      text-shadow: -2px 0 #00fff9, 2px 2px #ff00c1;
      animation: glitch-anim2 1s infinite linear alternate-reverse;
    }
  }
  @keyframes glitch-anim {
    $steps: 20;
    @for $i from 0 through $steps {
      #{percentage($i*(1/$steps))} {
        clip: rect(random(100)+px, 9999px, random(100)+px, 0);
        transform: skew((random(100) / 100) + deg);
      }
    }
  }
  @keyframes glitch-anim2 {
    $steps: 20;
    @for $i from 0 through $steps {
      #{percentage($i*(1/$steps))} {
        clip: rect(random(100)+px, 9999px, random(100)+px, 0);
        transform: skew((random(100) / 100) + deg);
      }
    }
  }
  @keyframes glitch-skew {
    $steps: 10;
    @for $i from 0 through $steps {
      #{percentage($i*(1/$steps))} {
        transform: skew((random(10) - 5) + deg);
      }
    }
  }
</style>
