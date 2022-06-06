<template>
  <BoxContainer>
    <template v-slot:row>
      <MainButton @onClick="handleVisibility" name="Toggle" />
    </template>
    <template v-slot:box>
      <ToggleBox v-if="visibleBox" />
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
