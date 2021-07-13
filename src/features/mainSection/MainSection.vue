<template>
  <div class="MainSection">
    <Header />
    <div class="MainSection_Content">
      <div class="MainSection_Text">
        <h1 class="MainSection_Title">
          Подписка на <br />
          Pro-Контент решает
        </h1>
        <h2 class="MainSection_Subtitle">
          Попробуйте 7 дней за 1€ при первой подписке
        </h2>
        <Button
          class="MainSection_Button"
          title="Узнать как"
          @click="onOpenModal()"
        />
        <Popup v-if="isVisibleModal" :onClose="() => onCloseModal()" />
      </div>
      <div class="Photo">
        <img class="Photo_Main" alt="Man" src="@/assets/man.png" />
        <Card
          class="Photo_Item1"
          title="Стремление попасть в окружение трейдеров"
        />
        <Card
          class="Photo_Item2"
          title="Отсутствие времени на отбор инструментов"
        />
        <Card class="Photo_Item3" title="Нехватку экспертности для торговли" />
      </div>
      <Button class="MobileButton" title="Узнать как" @click="onOpenModal()" />
    </div>
  </div>
</template>

<script>
import Header from "@/features/header/Header";
import Button from "@/components/Button/Button";
import Popup from "@/components/Popup/Popup";
import Card from "@/components/Card/Card";
export default {
  name: "MainSection",
  components: {
    Header,
    Button,
    Popup,
    Card,
  },
  data() {
    return {
      isVisibleModal: false,
    };
  },
  methods: {
    onOpenModal() {
      this.isVisibleModal = true;
    },
    onCloseModal() {
      this.isVisibleModal = false;
    },
  },
};
</script>

<style lang="scss">
@import "./mainSection.scss";
</style>
