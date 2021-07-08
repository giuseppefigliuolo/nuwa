<template>
  <router-link to="#">
    <button>
      {{ text }}
    </button>
  </router-link>
</template>

<script>
export default {
  props: ['text']
}
</script>

<style lang="scss" scoped>
  button{
    font-family: 'obviously', sans-serif;
    border: 1px solid rgba(255, 255, 255, 0.561);
    border-radius: 5px;
    padding: 1em;
    width: 100%;
    color: #fff;
    text-transform: capitalize;
    &:hover{
      background-color: #fff;
      color: #333;
      transition: 0.8s;
    }
  }
</style>
