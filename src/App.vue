<template>
  <h1>Hello {{ person }}</h1>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      person: "s",
    };
  },
});
</script>
