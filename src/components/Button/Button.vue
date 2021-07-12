<template>
  <button class="Button">
    {{ title }}
    <img class="HeaderItem_Icon" v-if="rightIcon" v-bind:src="rightIcon" />
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    title: String,
    rightIcon: String,
  },
};
</script>

<style lang="scss">
@import "./button.scss";
</style>
