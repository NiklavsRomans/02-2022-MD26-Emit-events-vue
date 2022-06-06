<template>
  <input class="checkbox" @change="handleCheck" type="checkbox" />
</template>

<script>
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "CheckBox",
  data() {
    return {};
  },
  emits: ["onCheck"],

  methods: {
    handleCheck() {
      this.$emit("onCheck");
    },
  },
});
</script>

<style scoped lang="scss">
@import "CheckBox.scss";
</style>
