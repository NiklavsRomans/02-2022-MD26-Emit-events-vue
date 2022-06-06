<template>
  <div class="box-container">
    <slot name="row"></slot>
    <div class="input-slot">
      <slot></slot>
    </div>
    <div class="box-slot">
      <slot name="box"></slot>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "BoxContainer",
  data() {
    return {};
  },
});
</script>

<style scoped lang="scss">
@import "BoxContainer.scss";
</style>
