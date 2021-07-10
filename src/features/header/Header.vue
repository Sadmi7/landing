<template>
  <div class="Header">
    <div class="Header_Number">
      <HeaderItem
        title="+7 958 581 57 68"
        :leftIcon="require('@/assets/phone.png')"
        :rightIcon="require('@/assets/orangeArrow.png')"
      />
    </div>
    <HeaderItem title="Сообщество трейдеров" />
    <HeaderItem title="Новости" />
    <HeaderItem title="Команда" />
    <HeaderItem title="Контакты" />
    <HeaderItem title="Роман" :leftIcon="require('@/assets/user.png')" />
  </div>
</template>

<script>
import HeaderItem from "@/components/HeaderItem/HeaderItem";
export default {
  name: "Header",
  components: {
    HeaderItem,
  },
};
</script>

<style lang="scss">
@import "./header.scss";
</style>
