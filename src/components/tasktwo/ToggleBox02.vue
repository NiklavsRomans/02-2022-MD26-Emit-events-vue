<template>
  <BoxContainer>
    <template v-slot:row>
      <CheckBox @onCheck="handleVisibility" />
    </template>
    <template v-slot:box>
      <ToggleBox :classname="boxClass" />
    </template>
  </BoxContainer>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";
import BoxContainer from "@/components/reusablecomponents/boxcontainer/BoxContainer.vue";
import ToggleBox from "@/components/reusablecomponents/togglebox/ToggleBox.vue";
import CheckBox from "@/components/reusablecomponents/checkbox/CheckBox.vue";

export default defineComponent({
  components: {
    BoxContainer,
    ToggleBox,
    CheckBox,
  },
  name: "ToggleBox02",
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
