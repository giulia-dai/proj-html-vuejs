<script>
import AppNav from "./components/AppNav.vue";
import AppJumbo from "./components/AppJumbo.vue";
import AboutUsSection from "./components/AboutUsSection.vue";
import HelpSection from "./components/HelpSection.vue";
import CoursesSection from "./components/CoursesSection.vue";
import VideoSection from "./components/VideoSection.vue";
import EventSection from "./components/EventSection.vue";
import ReviewSection from "./components/ReviewSection.vue";
import FooterTop from "./components/FooterTop.vue";
import FooterBottom from "./components/FooterBottom.vue";

export default {
  components: {
    AppNav,
    AppJumbo,
    AboutUsSection,
    HelpSection,
    CoursesSection,
    VideoSection,
    EventSection,
    ReviewSection,
    FooterTop,
    FooterBottom
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
    <CoursesSection></CoursesSection>
    <VideoSection></VideoSection>
    <EventSection></EventSection>
    <ReviewSection></ReviewSection>
  </main>
  <!-- qui inizia il footer -->
  <footer>
    <FooterTop></FooterTop>
    <FooterBottom></FooterBottom>
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
