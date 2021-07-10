<template>
  <div class="HeaderItem">
    <img class="HeaderItem_Icon" v-if="leftIcon" v-bind:src="leftIcon" />
    <div>{{ title }}</div>
    <img class="HeaderItem_Icon" v-if="rightIcon" v-bind:src="rightIcon" />
  </div>
</template>

<script>
export default {
  name: "HeaderItem",
  props: {
    leftIcon: String,
    rightIcon: String,
    title: String,
  },
};
</script>

<style lang="scss">
@import "./HeaderItem";
</style>
