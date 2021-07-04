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
    border: 1px solid #fff;
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
