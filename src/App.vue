<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <section class="main-view">
          <InputBox01 />
          <InputBox02 />
          <InputBox03 />
          <InputBox04 />
          <TextBox01 />
          <TextBox02 />
          <ToggleBox01 />
          <ToggleBox02 />
        </section>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

//TASK ONE IMPORTS
import InputBox01 from "./components/taskone/InputBox01.vue";
import InputBox02 from "./components/taskone/InputBox02.vue";
import InputBox03 from "./components/taskone/InputBox03.vue";
import InputBox04 from "./components/taskone/InputBox04.vue";

// TASK TWO IMPORTS
import TextBox01 from "./components/tasktwo/TextBox01.vue";
import TextBox02 from "./components/tasktwo/TextBox02.vue";
import ToggleBox01 from "./components/tasktwo/ToggleBox01.vue";
import ToggleBox02 from "./components/tasktwo/ToggleBox02.vue";
export default defineComponent({
  name: "App",
  components: {
    InputBox01,
    InputBox02,
    InputBox03,
    InputBox04,
    TextBox01,
    TextBox02,
    ToggleBox01,
    ToggleBox02,
  },
  data: () => {
    return {};
  },
});
</script>

<style lang="scss">
.main-view {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  gap: 50px;
}
</style>
