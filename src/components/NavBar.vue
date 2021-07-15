<template>
  <nav>
    <div class="logo">
      <img :src="require('../assets/svg/nuwa_logo_bianco.png')" alt="logo-nuwa" />
    </div>
    <div class="menu">
      <ul>
        <li v-for="(item, i) in menuItems" :key="item + i" class="h-font">
          <router-link :to="{ name: item.link }">{{ item.name }}</router-link>
        </li>
      </ul>
    </div>
    <div class="countdown d-flex justify-center">
      <Countdown :compact="true" :fontSize="'1rem'" />
    </div>
  </nav>
</template>

<script>
import Countdown from './Countdown.vue'

export default {
  components: { Countdown },
  data() {
    return {
      menuItems: [
        {
          name: 'Capsula',
          link: 'Home'
        },
        {
          name: 'Marte',
          link: 'Marte'
        },
        {
          name: 'Contatti',
          link: 'Contact'
        }
      ]
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
  width: 100%;
  padding: 0.8rem 4rem;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

.countdown {
  width: 300px;
}

a {
  color: white !important;
}
.menu ul {
  display: flex;
  font-size: 1rem;
  li {
    padding: 0 2em;
    cursor: pointer;
  }
}
@media screen and (max-width: 700px) {
  nav {
    flex-direction: column;
    padding: 1em;
    .menu ul li {
      padding: 1em;
    }
  }
}
</style>
