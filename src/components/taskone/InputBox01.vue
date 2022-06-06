<template>
  <BoxContainer>
    <h2 class="title">{{ title }}</h2>
    <InputTextBox placeholder="Change title.." v-model="inputValue">
      <MainButton @onClick="handleTitle" name="Change" />
    </InputTextBox>
  </BoxContainer>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";
import BoxContainer from "@/components/reusablecomponents/boxcontainer/BoxContainer.vue";
import InputTextBox from "@/components/reusablecomponents/inputtext/InputText.vue";
import MainButton from "@/components/reusablecomponents/mainbutton/MainButton.vue";

export default defineComponent({
  components: {
    BoxContainer,
    InputTextBox,
    MainButton,
  },
  name: "InputBox01",
  data() {
    return {
      title: "Title",
      inputValue: "",
    };
  },

  methods: {
    handleTitle() {
      this.title = this.inputValue;
      this.inputValue = "";
    },
  },
});
</script>
<style lang="scss">
.title {
  text-align: center;
  font-size: 26px;
  padding-bottom: 10px;
}
</style>
