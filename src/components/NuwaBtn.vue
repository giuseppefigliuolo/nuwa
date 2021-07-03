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

<style lang="scss" scoped></style>
