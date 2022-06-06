<template>
  <BoxContainer>
    <InputTextBox placeholder="Update title.." v-model="inputTitleValue">
      <MainButton @onClick="handleTitle" name="Change" />
    </InputTextBox>
    <br />
    <InputTextBox
      placeholder="Update description"
      v-model="inputDescriptionValue"
    >
      <MainButton @onClick="handleDescription" name="Change" />
    </InputTextBox>
    <template v-slot:box>
      <TextBox :title="title" :description="description" />
    </template>
  </BoxContainer>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";
import BoxContainer from "@/components/reusablecomponents/boxcontainer/BoxContainer.vue";
import InputTextBox from "@/components/reusablecomponents/inputtext/InputText.vue";
import MainButton from "@/components/reusablecomponents/mainbutton/MainButton.vue";
import TextBox from "@/components/reusablecomponents/textbox/TextBox.vue";

export default defineComponent({
  components: {
    BoxContainer,
    InputTextBox,
    MainButton,
    TextBox,
  },
  name: "DescriptionBox01",
  data() {
    return {
      title: "Title",
      description: "Description",
      inputTitleValue: "",
      inputDescriptionValue: "",
    };
  },

  methods: {
    handleTitle() {
      this.title = this.inputTitleValue;
      this.inputTitleValue = "";
    },

    handleDescription() {
      this.description = this.inputDescriptionValue;
      this.inputDescriptionValue = "";
    },
  },
});
</script>
<style></style>
