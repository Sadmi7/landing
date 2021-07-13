<template>
  <div>
    <input
      type="text"
      :class="isError ? 'InputError' : 'Input'"
      :placeholder="placeholder"
    />
    <span class="ErrorText">{{ isError ? errorText : "" }}</span>
  </div>
</template>

<script>
export default {
  name: "Input",
  props: {
    placeholder: String,
    isError: Boolean,
    errorText: String,
  },
};
</script>

<style lang="scss">
@import "./input.scss";
</style>
