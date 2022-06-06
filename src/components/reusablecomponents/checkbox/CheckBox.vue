<template>
  <input class="checkbox" @change="$emit('onCheck')" type="checkbox" />
</template>

<script>
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "CheckBox",
  data() {
    return {};
  },
  emits: ["onCheck"],
});
</script>

<style scoped lang="scss">
@import "CheckBox.scss";
</style>
