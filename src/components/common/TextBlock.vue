<template>
  <div class="text-block">
    <slot class="special-title" name="special-title"></slot>
    <h1 class="text-block__title">{{ title }}</h1>
    <slot name="text" class="text-block__text"></slot>
  </div>
</template>

<script>
export default {
  mounted() {
    if (this.$slots['special-title']) {
      console.log('Слот special-title передан!');
    }
  },
  props: {
    title: String,
    text: String,
  },
};
</script>

<style scoped lang="scss">
.text-block {
  max-width: 800px;
  height: 100vh;
  margin: 0 auto;
  margin-bottom: 8.3333vw;
  box-sizing: inherit;

  .text-block__title {
    font-family: 'Futura PT Medium', sans-serif;
    font-size: 3rem;
    margin-bottom: 21px;
  }

  .text-block__text {
    font-family: 'Futura PT Book', sans-serif;
    font-size: 2rem;
  }
}
</style>
