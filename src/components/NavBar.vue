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
      <Countdown :compact="true" fontSize="1.5rem" />
    </div>
  </nav>
</template>

<script>
import Countdown from './Countdown.vue'

export default {
  components: { Countdown },
  data() {
    return {
      menuItems: ['Capsula', 'Marte', 'Contatti']
    }
  }
}
</script>

<style lang="scss" scoped>
nav {
  position: fixed;
  background-color: #202120;
  z-index: 100;
  top: 0;
  left: 0;
  width: 100vw;
  padding: 0.8rem 4rem;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items:center ;
}

.menu ul {
  display: flex;
  font-size: 1rem;
  li{
    padding: 0 2em;
  }
}
</style>
