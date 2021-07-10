<template>
  <div class="InfoSection">
    <div class="InfoSection_MainText">
      Но с другой <br />
      стороны...
    </div>
    <div class="Graph">
      <img
        class="BusinessGraphic"
        alt="BusinessGraphic"
        src="@/assets/graph.png"
      />
      <img
        class="Businessman"
        alt="Businessman"
        src="@/assets/businessman.png"
      />
      <div class="InfoSection_Text">
        <img class="InfoSection_Image" alt="Info" src="@/assets/info.png" />
        Спустя пол года наступает выгорание и мысль “а может бросить это всё”
        берёт верх, хотя по факту начиналось всё хорошо
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "InfoSection",
};
</script>

<style lang="scss">
/* eslint-disable */
@import "./infoSection.scss";
</style>
