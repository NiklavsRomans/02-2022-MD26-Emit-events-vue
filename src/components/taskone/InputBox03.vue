<template>
  <BoxContainer>
    <InputTextBox placeholder="Change box color.." v-model="inputValue">
      <MainButton @onClick="changeColor" name="Change" />
    </InputTextBox>
    <template v-slot:box>
      <ColorBox :color="color" />
    </template>
  </BoxContainer>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";
import BoxContainer from "@/components/reusablecomponents/boxcontainer/BoxContainer.vue";
import InputTextBox from "@/components/reusablecomponents/inputtext/InputText.vue";
import MainButton from "@/components/reusablecomponents/mainbutton/MainButton.vue";
import ColorBox from "@/components/reusablecomponents/colorbox/ColorBox.vue";

export default defineComponent({
  components: {
    BoxContainer,
    InputTextBox,
    MainButton,
    ColorBox,
  },
  name: "InputBox03",
  data() {
    return {
      title: "Change Color",
      color: "",
      inputValue: "",
    };
  },

  methods: {
    changeColor() {
      this.color = this.inputValue;
      this.inputValue = "";
    },
  },
});
</script>
<style></style>
