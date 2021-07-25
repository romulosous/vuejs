<template>
  <h1>{{ name }} {{ lastname }}</h1>
  <h1>{{ fullName }}</h1>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      name: "Romim",
      lastname: "Carvalho",
    };
  },
  computed: {
    fullName(): string {
      return `${this.name} ${this.lastname}`;
    },
  },
});
</script>
