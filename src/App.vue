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
h1,
h2,
h3,
h4,
h5 {
  font-family: 'obviously-wide', sans-serif !important;
  font-weight: 600;
}

p {
  font-family: 'obviously', sans-serif;
}

.h-font {
  font-family: 'obviously-wide', sans-serif !important;
  font-weight: 500;
}

.p-font {
  font-family: 'obviously', sans-serif;
}
</style>
