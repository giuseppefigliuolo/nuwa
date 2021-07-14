<template>
  <router-link to="#">
    <button class="button"> {{text}}
      <span class="top"></span>
      <span class="left"></span>
      <span class="bottom"></span>
      <span class="right"></span>
    </button>
  </router-link>
</template>

<script>
export default {
  props: ['text', 'link']
}
</script>

<style lang="scss" scoped>
  button{
    font-family: 'obviously', sans-serif;
  }
  .button {
    position: relative;
    display: inline-block;
    padding: 1.5em;
    margin: 2em 0;
    color: #70C3BB;
    font-size: 1em;
    text-decoration: none;
    text-transform: uppercase;
    transition: 0.5s;
    letter-spacing: 4px;
    overflow: hidden;
  }

.button:hover{
  border: 2px solid;
  box-shadow: 0 0 5px ;
}
.button span {
  position: absolute;
  display: block;
}

.top {
  top:0;
  left:-100%;
  width: 100%;
  height: 2px;
  background: linear-gradient(90deg, transparent, #70C3BB);
  animation: animate1 1s linear infinite;
}

@keyframes animate1
{
  0%
  {
    left: -100%;
  }
  50%, 100%
  {
    left: 100%;
  }
}

.right {
  top:-100%;
  right: 0;
  width: 2px;
  height: 100%;
  background: linear-gradient(180deg, transparent, #70C3BB);
  animation: animate2 1s linear infinite;
  animation-delay: 0.25s;
}

@keyframes animate2
{
  0%
  {
    top: -100%;
  }
  50%, 100%
  {
    top: 100%;
  }
}

.bottom {
  bottom:0;
  right: -100%;
  width: 100%;
  height: 2px;
  background: linear-gradient(270deg, transparent, #70C3BB);
  animation: animate3 1s linear infinite;
  animation-delay: 0.5s;
}

@keyframes animate3
{
  0%
  {
    right: -100%;
  }
  50%, 100%
  {
    right: 100%;
  }
}

.left {
  bottom:-100%;
  left: 0;
  width: 2px;
  height: 100%;
  background: linear-gradient(360deg, transparent, #70C3BB);
  animation: animate4 1s linear infinite;
  animation-delay: 0.75s;
}

@keyframes animate4
{
  0%
  {
    bottom: -100%;
  }
  50%, 100%
  {
    bottom: 100%;
  }
}
</style>
