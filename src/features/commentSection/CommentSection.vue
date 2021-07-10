<template>
  <div class="CommentSection">
    <div class="CommentSection_MainText">
      <div>
        Отзывы подписчиков <br />
        и их результаты
      </div>
      <Button
        class="CommentSection_Button"
        title="Больше отзывов"
        :rightIcon="require('@/assets/rightArrow.png')"
      />
    </div>
    <div class="CommentSection_MainContent">
      <Button title="Хочу как они" />
      <div>
        <img alt="Circle" src="@/assets/circle.png" />
      </div>
      <div>
        <Slider />
      </div>
    </div>
  </div>
</template>

<script>
import Button from "@/components/Button/Button";
import Slider from "@/components/Slider/Slider";
export default {
  name: "CommentSection",
  components: {
    Button,
    Slider,
  },
};
</script>

<style lang="scss">
@import "commentSection.scss";
</style>
