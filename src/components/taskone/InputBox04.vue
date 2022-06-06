<template>
  <BoxContainer>
    <InputTextBox placeholder="Change box color.." v-model="inputValue" />
    <template v-slot:box>
      <ColorBox :color="updateColor" />
    </template>
  </BoxContainer>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";
import BoxContainer from "@/components/reusablecomponents/boxcontainer/BoxContainer.vue";
import InputTextBox from "@/components/reusablecomponents/inputtext/InputText.vue";
import ColorBox from "@/components/reusablecomponents/colorbox/ColorBox.vue";

export default defineComponent({
  components: {
    BoxContainer,
    InputTextBox,
    ColorBox,
  },
  name: "InputBox04",
  data() {
    return {
      title: "Change Color",
      color: "",
      inputValue: "",
    };
  },

  computed: {
    updateColor() {
      if (!this.inputValue) {
        return this.color;
      }
      return this.inputValue;
    },
  },
});
</script>
<style></style>
