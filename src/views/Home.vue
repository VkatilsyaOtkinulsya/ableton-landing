<template>
  <div class="app-container">
    <Header></Header>
    <HeroSection></HeroSection>
    <ContentSection></ContentSection>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from '@/components/layout/Header.vue'
import Footer from '@/components/layout/Footer.vue'
import HeroSection from '@/components/sections/HeroSection.vue'
import ContentSection from '@/components/sections/ContentSection.vue'

export default {
  components: {
    Footer,
    Header,
    HeroSection,
    ContentSection,
  },
  data() {},
}
</script>

<style scoped>
.container {
  background-color: var(--vt-c-white);
}
</style>
