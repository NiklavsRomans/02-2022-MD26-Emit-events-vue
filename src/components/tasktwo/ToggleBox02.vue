<template>
  <BoxContainer>
    <template v-slot:row>
      <CheckBox @onCheck="handleVisibility" />
    </template>
    <template v-slot:box>
      <ToggleBox v-if="visibleBox" />
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
      visibleBox: true,
    };
  },

  methods: {
    handleVisibility() {
      this.visibleBox = !this.visibleBox;
    },
  },
});
</script>
<style></style>
