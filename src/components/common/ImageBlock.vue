<template>
  <div class="image-block">
    <div v-if="normalizedImages.length" class="images-container">
      <img
        v-for="(image, index) in normalizedImages"
        :key="index"
        :src="image"
        :alt="`Image ${index + 1}`"
        class="image"
      />
    </div>

    <div v-if="hasColorBlock" class="color-block">
      <slot name="color-block-content">
        <p v-if="colorBlockText" class="color-block-text">{{ colorBlockText }}</p>
      </slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    images: {
      type: [Array, String],
      default: () => [],
    },
    color: {
      type: String,
      default: '',
    },
    colorBlockText: {
      type: String,
      default: '',
    },
  },
  computed: {
    hasColorBlock() {
      return !!this.color || this.$slots['color-block-content'];
    },
    normalizedImages() {
      return typeof this.images === 'string' ? [this.images] : this.images;
    },
  },
};
</script>

<style scoped lang="scss">
.image-block {
  display: flex;
  align-items: center;

  .image {
    max-width: 100%;
    height: auto;
  }
}
</style>
