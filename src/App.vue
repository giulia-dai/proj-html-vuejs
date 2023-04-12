<script>
import AppNav from "./components/AppNav.vue";
import AppJumbo from "./components/AppJumbo.vue";
import AboutUsSection from "./components/AboutUsSection.vue";
import HelpSection from "./components/HelpSection.vue";

export default {
  components: {
    AppNav,
    AppJumbo,
    AboutUsSection,
    HelpSection,
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
    <AboutUsSection></AboutUsSection>
    <HelpSection></HelpSection>
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

footer {
  clear: left;
}
</style>
