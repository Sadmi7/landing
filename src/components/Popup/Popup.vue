<template>
  <div class="Popup">
    <div class="PopupFreeSpace" @click="onClose"></div>
    <div class="Popup_Text">
      <div class="Popup_Title">Введите ваши данные</div>
      <div class="Popup_Subtitle">для оформления дocтупа на PRO-контент</div>
      <div class="Popup_Input">
        <Input
          :value="name"
          :isError="isEmptyName"
          errorText="Name can't be blank"
          @change="(e) => (name = e.target.value)"
          placeholder="Имя"
        />
        <Input
          :value="email"
          :isError="isEmptyEmail"
          :errorText="emailErrorMessage"
          @change="(e) => (email = e.target.value)"
          placeholder="Email"
        />
        <Input
          type="number"
          :value="phoneNumber"
          :isError="isEmptyPhoneNumber"
          :errorText="phoneNumberErrorMessage"
          @change="(e) => (phoneNumber = e.target.value)"
          placeholder="+380"
        />
        <div class="Popup_Privacy">
          <input
            id="checkbox"
            type="checkbox"
            class="Popup_Checkbox"
            :v-model="!checked"
          />

          <label for="checkbox" :style="checked ? 'color: white' : 'color:red'">
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
      checked: true,
      isEmptyName: false,
      isEmptyEmail: false,
      emailErrorMessage: "",
      isEmptyPhoneNumber: false,
      phoneNumberErrorMessage: "",
    };
  },

  methods: {
    onValidateInputs() {
      if (this.name === "") {
        this.isEmptyName = true;
      } else {
        this.isEmptyName = false;
      }

      if (this.email === "") {
        this.isEmptyEmail = true;
        this.emailErrorMessage = "Email can't be blank";
      }

      if (!this.email.includes("@") && this.email !== "") {
        this.isEmptyEmail = true;
        this.emailErrorMessage = "Email should contain @";
      }

      if (this.email.includes("@") && this.email !== "") {
        this.isEmptyEmail = false;
      }

      if (this.phoneNumber === "") {
        this.isEmptyPhoneNumber = true;
        this.phoneNumberErrorMessage = "Phone number can't be blank";
      }

      if (!this.phoneNumber.includes("+380") && this.phoneNumber !== "") {
        this.isEmptyPhoneNumber = true;
        this.phoneNumberErrorMessage = "Phone number should start from +380";
      }

      if (this.phoneNumber.includes("+380") && this.phoneNumber !== "") {
        this.isEmptyPhoneNumber = false;
      }

      if (this.checked) {
        this.checked = false;
      } else {
        this.checked = true;
      }

      if (
        this.name !== "" &&
        this.email.includes("@") &&
        this.phoneNumber.includes("+380") &&
        this.checked
      ) {
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
