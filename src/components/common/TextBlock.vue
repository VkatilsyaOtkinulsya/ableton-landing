<template>
  <div class="text-block">
    <h1 class="text-block__title"><slot name="title"></slot></h1>
    <p class="text-block__text"><slot name="text"></slot></p>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    text: String,
  },
}
</script>

<style scoped lang="scss">
.text-block {
  width: 50vw;
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
