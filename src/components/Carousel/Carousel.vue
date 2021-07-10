<template>
  <div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      index: 0,
      slides: [],
    };
  },
  mounted() {
    this.slides = this.$children;
  },
};
</script>

<style lang="scss">
@import "./carousel.scss";
</style>
