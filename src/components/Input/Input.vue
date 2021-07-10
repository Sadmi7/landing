<template>
  <div>
    <input type="text" class="Input" :placeholder="placeholder" />
  </div>
</template>

<script>
export default {
  name: "Input",
  props: {
    placeholder: String,
  },
};
</script>

<style lang="scss">
@import "./input.scss";
</style>
