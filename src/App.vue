<script>
import AppNav from "./components/AppNav.vue";

export default {
  components: {
    AppNav,
  },

  data() {

  },
}

</script>

<template>
  <!-- qui inizia l'header -->
  <header>
    <AppNav></AppNav>
  </header>
  <!-- qui inizia il main -->
  <main>
    <h1>main</h1>
  </main>
  <!-- qui inizia il footer -->
  <footer>
    <h1>footer</h1>
  </footer>
</template>

<style lang="scss">
h1 {
  color: red;
}
</style>
