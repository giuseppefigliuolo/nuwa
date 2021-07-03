<template>
  <nav>
    <div class="logo">
      <img :src="require('../assets/logo.svg')" alt="" />
    </div>
    <div class="menu">
      <ul>
        <li v-for="item in menuItems" :key="item" class="h-font">{{ item }}</li>
      </ul>
    </div>
    <div class="countdown d-flex justify-center">
      <p class="h-font">6mesi 20giorni 11h 32min 10s</p>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      menuItems: ['Capsula', 'Marte', 'Contact']
    }
  }
}
</script>

<style lang="scss" scoped>
nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  padding: 0.8rem 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}

.menu ul {
  display: flex;
  justify-content: space-evenly;
  font-size: 0.9rem;
}
</style>
