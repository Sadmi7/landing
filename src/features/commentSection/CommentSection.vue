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
      <div class="CommentSection_Slider">
        <Slider />
      </div>
      <div class="Circle"></div>
    </div>
    <div class="CommentSection_FooterButton">
      <Button title="Хочу как они" />
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
