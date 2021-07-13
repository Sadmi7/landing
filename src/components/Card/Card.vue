<template>
  <div class="Card">
    <div class="Card_Item">
      <div class="Card_Header">
        Now
      </div>
      <div class="Card_Title">
        {{ title }}
      </div>
    </div>
    <div class="Card_Backdrop"></div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    title: String,
  },
};
</script>

<style lang="scss">
@import "./card.scss";
</style>
