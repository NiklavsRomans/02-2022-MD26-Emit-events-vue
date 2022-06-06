<template>
  <BoxContainer>
    <template v-slot:row>
      <MainButton @onClick="handleVisibility" name="Toggle" />
    </template>
    <template v-slot:box>
      <ToggleBox :classname="boxClass" />
    </template>
  </BoxContainer>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";
import BoxContainer from "@/components/reusablecomponents/boxcontainer/BoxContainer.vue";
import MainButton from "@/components/reusablecomponents/mainbutton/MainButton.vue";
import ToggleBox from "@/components/reusablecomponents/togglebox/ToggleBox.vue";

export default defineComponent({
  components: {
    BoxContainer,
    MainButton,
    ToggleBox,
  },
  name: "ToggleBox01",
  data() {
    return {
      boxClass: "box",
    };
  },

  methods: {
    handleVisibility() {
      if (this.boxClass === "box") {
        return (this.boxClass = "hidden");
      } else {
        return (this.boxClass = "box");
      }
    },
  },
});
</script>
<style></style>
