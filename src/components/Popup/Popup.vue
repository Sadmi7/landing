<template>
  <div class="Popup">
    <div class="PopupFreeSpace" @click="onClose"></div>
    <div class="Popup_Text">
      <div class="Popup_Title">Введите ваши данные</div>
      <div class="Popup_Subtitle">для оформления дocтупа на PRO-контент</div>
      <div class="Popup_Input">
        <Input
          :value="name"
          @change="(e) => (name = e.target.value)"
          placeholder="Имя"
        />
        <Input
          :value="email"
          @change="(e) => (email = e.target.value)"
          placeholder="Email"
        />
        <Input
          type="number"
          :value="phoneNumber"
          @change="(e) => (phoneNumber = e.target.value)"
          placeholder="+380"
        />
        <div class="Popup_Privacy">
          <input
            id="checkbox"
            type="checkbox"
            class="Popup_Checkbox"
            v-model="checked"
          />

          <label for="checkbox">
            Я прочел(-ла) и принимаю Условия подписки и Политику
            конфиденциальности
          </label>
        </div>
        <Button title="Продолжить" @click="onValidateInputs" />
      </div>
    </div>
  </div>
</template>

<script>
import Input from "@/components/Input/Input";
import Button from "@/components/Button/Button";
export default {
  name: "Popup",
  components: { Input, Button },
  props: ["onClose"],
  data() {
    return {
      name: "",
      email: "",
      phoneNumber: "",
      checked: false,
    };
  },

  methods: {
    onValidateInputs() {
      if (
        this.name === "" ||
        !this.email.includes("@") ||
        !this.phoneNumber.includes("+380") ||
        !this.checked
      ) {
        alert("Должны быть заполнены все поля");
      } else {
        const data = {
          name: this.name,
          email: this.email,
          phoneNumber: this.phoneNumber,
          isChecked: this.checked,
        };
        console.log(data);
        this.onClose();
      }
    },
  },
  mounted() {
    document.body.style.overflow = "hidden";
  },
  unmounted() {
    document.body.style.overflow = "auto";
  },
};
</script>

<style lang="scss">
@import "./popup.scss";
</style>
