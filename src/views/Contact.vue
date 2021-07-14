<template>
  <section>
    <div id="wrapper">
      <h3 class="glitch" data-text="Le iscrizioni apriranno tra...">Le iscrizioni apriranno tra...</h3>
	  </div>
    <countdown fontSize="2.8rem" />
  </section>
</template>

<script>
import countdown from '../components/Countdown.vue'
import HeroSection from '../components/HeroSection.vue'
export default {
  components: { countdown, HeroSection }
}
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  h3{
    padding-bottom: 3em;
  }
}
// glitch effect
#wrapper {
    text-align: left;
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
    color: #E7393E ;
    font-size: 2em;
    letter-spacing: .5em;
    animation: glitch-skew 1s infinite linear alternate-reverse;
    &::before{
      @include glitchCopy;
      left: 2px;
      text-shadow: -2px 0 #70C3BB;
      clip: rect(44px, 450px, 56px, 0);
      animation: glitch-anim 5s infinite linear alternate-reverse;
    }
    &::after {
      @include glitchCopy;
      left: -2px;
      text-shadow: -2px 0 #F49911, 2px 2px #70C3BB;
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
