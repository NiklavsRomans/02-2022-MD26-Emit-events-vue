<template>
  <button class="button" @click="handleClick">{{ name }}</button>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "MainButton",
  props: ["name"],
  emits: ["onClick"],
  methods: {
    handleClick() {
      this.$emit("onClick");
    },
  },
});
</script>

<style scoped lang="scss">
@import "MainButton.scss";
</style>
