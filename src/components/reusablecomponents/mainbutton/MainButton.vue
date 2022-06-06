<template>
  <button class="button" @click="$emit('onClick')">{{ name }}</button>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "MainButton",
  props: ["name"],
  emits: ["onClick"],
});
</script>

<style scoped lang="scss">
@import "MainButton.scss";
</style>
