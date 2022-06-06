<template>
  <div :style="{ 'background-color': color }" class="color-box"></div>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "ColorBox",
  props: ["color"],
});
</script>

<style scoped lang="scss">
@import "ColorBox.scss";
</style>
