<template>
  <BoxContainer>
    <h2 class="title">{{ updateTitle }}</h2>
    <InputTextBox placeholder="Change title.." v-model="inputValue" />
  </BoxContainer>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";
import BoxContainer from "@/components/reusablecomponents/boxcontainer/BoxContainer.vue";
import InputTextBox from "@/components/reusablecomponents/inputtext/InputText.vue";

export default defineComponent({
  components: {
    BoxContainer,
    InputTextBox,
  },
  name: "InputBox01",
  data() {
    return {
      title: "Title",
      inputValue: "",
    };
  },
  computed: {
    updateTitle() {
      if (!this.inputValue) {
        return this.title;
      }
      return this.inputValue;
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
