<template>
  <div class="MainSection">
    <Header />
    <div class="MainSection_Content">
      <div class="MainSection_Text">
        <div class="MainSection_TextWrapper">
          <h1 class="MainSection_Title">
            Подписка на <br />
            Pro-Контент решает
          </h1>
          <h2 class="MainSection_Subtitle">
            Попробуйте 7 дней за 1€ при первой подписке
          </h2>
          <Button class="MainSection_Button" title="Узнать как" />
          <!-- <Popup /> -->
        </div>
      </div>
      <div class="Photo">
        <img class="Photo_Main" alt="Man" src="@/assets/man.png" />
        <img class="Photo_Item1" alt="Problem1" src="@/assets/problem1.png" />
        <img class="Photo_Item2" alt="Problem2" src="@/assets/problem2.png" />
        <img class="Photo_Item3" alt="Problem3" src="@/assets/problem3.png" />
      </div>
    </div>
  </div>
</template>

<script>
import Header from "@/features/header/Header";
import Button from "@/components/Button/Button";
// import Popup from "@/components/Popup/Popup";
export default {
  name: "MainSection",
  components: {
    Header,
    Button,
    // Popup,
  },
};
</script>

<style lang="scss">
@import "./mainSection.scss";
</style>
