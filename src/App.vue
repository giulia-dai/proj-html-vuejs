<script>
import AppNav from "./components/AppNav.vue";
import AppJumbo from "./components/AppJumbo.vue";

export default {
  components: {
    AppNav,
    AppJumbo,
  },

  data() {

  },
}

</script>

<template>
  <!-- qui inizia l'header -->
  <header>
    <div class="container">
      <AppNav></AppNav>
    </div>
    <AppJumbo></AppJumbo>
  </header>

  <!-- qui inizia il main -->
  <main>
    <h1>qui inizia il main</h1>
  </main>
  <!-- qui inizia il footer -->
  <footer>
    <h1>footer</h1>
  </footer>
</template>

<style lang="scss">
.container {
  max-width: 1250px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
}
</style>
