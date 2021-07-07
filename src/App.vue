<template>
  <v-app>
    <nav-bar />
    <main>
      <router-view />
    </main>
  </v-app>
</template>

<script>
import NavBar from './components/NavBar.vue'

export default {
  name: 'App',
  components: { NavBar },
  data: () => ({
    //
  })
}
</script>

<style lang="scss">
.v-application--wrap {
  background-color: #212021;
  color: white;
}

li {
  list-style-type: none;
}

a {
  text-decoration: none;
}

h2,
h3,
h4,
h5 {
  font-family: 'obviously', sans-serif !important;
}

p {
  font-family: 'Chakra Petch', sans-serif;
}

.h-font {
  font-family: 'obviously', sans-serif !important;
}

.p-font {
  font-family: 'Chakra Petch', sans-serif;
}
</style>
