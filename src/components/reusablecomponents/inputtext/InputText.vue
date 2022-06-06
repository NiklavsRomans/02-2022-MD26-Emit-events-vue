<template>
  <div class="input-container">
    <input
      class="input"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      type="text"
      :placeholder="placeholder"
    />
    <slot></slot>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "InputTextBox",
  props: ["modelValue", "placeholder"],
  emits: ["update:modelValue"],
});
</script>

<style scoped lang="scss">
@import "InputText.scss";
</style>
