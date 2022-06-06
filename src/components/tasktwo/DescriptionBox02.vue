<template>
  <BoxContainer>
    <InputTextBox placeholder="Update title.." v-model="inputTitleValue">
    </InputTextBox>
    <br />
    <InputTextBox
      placeholder="Update description"
      v-model="inputDescriptionValue"
    >
    </InputTextBox>
    <template v-slot:box>
      <TextBox :title="changeTitle" :description="changeDescription" />
    </template>
  </BoxContainer>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";
import BoxContainer from "@/components/reusablecomponents/boxcontainer/BoxContainer.vue";
import InputTextBox from "@/components/reusablecomponents/inputtext/InputText.vue";
import TextBox from "@/components/reusablecomponents/textbox/TextBox.vue";

export default defineComponent({
  components: {
    BoxContainer,
    InputTextBox,
    TextBox,
  },
  name: "DescriptionBox02",
  data() {
    return {
      title: "Title",
      description: "Description",
      inputTitleValue: "",
      inputDescriptionValue: "",
    };
  },

  computed: {
    changeTitle() {
      if (!this.inputTitleValue) {
        return this.title;
      }
      return this.inputTitleValue;
    },

    changeDescription() {
      if (!this.inputDescriptionValue) {
        return this.description;
      }
      return this.inputDescriptionValue;
    },
  },
});
</script>
<style></style>
