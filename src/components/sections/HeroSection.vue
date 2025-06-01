<template>
  <div class="hero-section-wrapper">
    <HeroIcon class="hero-logo" />
  </div>
</template>

<script>
import HeroIcon from '@/components/icons/HeroIcon.vue'

export default {
  components: {
    HeroIcon,
  },
}
</script>

<style scoped lang="scss">
.hero-section-wrapper {
  background-image: url('https://ableton-production.imgix.net/about/header.jpg?auto=format&dpr=0.67&fit=crop&fm=jpg&h=719&ixjsv=1.1.3&w=1333');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 50% 50%;
  min-height: calc(100vh - 120px);

  .hero-logo {
    position: absolute;
    top: 62%;
    left: 50%;
  }
}

@media screen and (min-width: 100rem) {
  .hero-section-wrapper {
    margin-right: 133.333px;
    margin-left: 133.333px;
    margin-bottom: 133.333px;
  }
}

@media screen and (min-width: 48rem) {
  .hero-logo {
    margin-left: -215px;
    margin-top: -52px;
  }
}
</style>
