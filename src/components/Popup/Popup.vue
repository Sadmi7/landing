<template>
  <div class="Popup">
    <div class="Popup_Text">
      <slot />
      <div class="Popup_Title">Введите ваши данные</div>
      <div class="Popup_Subtitle">для оформления дocтупа на PRO-контент</div>
      <div class="Popup_Input">
        <Input placeholder="Имя" />
        <Input placeholder="Email" />
        <Input placeholder="+380" />
        <div>
          <div>У меня есть аккаунт</div>
          <div>
            <img alt="User" src="@/assets/user.png" />
            Войти
          </div>
        </div>
      </div>

      <div></div>
      <button>Close</button>
    </div>
  </div>
</template>

<script>
import Input from "@/components/Input/Input";
export default {
  components: { Input },
  name: "Popup",
};
</script>

<style lang="scss">
@import "./popup.scss";
</style>
