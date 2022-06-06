<template>
  <div :class="classname"></div>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "ToogleBox",
  props: ["classname"],
  data() {
    return {};
  },
});
</script>

<style scoped lang="scss">
@import "ToggleBox.scss";
</style>
