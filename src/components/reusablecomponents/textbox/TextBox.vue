<template>
  <div class="text-box">
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
  </div>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
  name: "TextBox",
  props: ["title", "description"],
});
</script>

<style scoped lang="scss">
@import "TextBox.scss";
</style>
