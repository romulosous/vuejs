<template>
  <h2>{{ name }} {{ lastname }}</h2>
  <h2>{{ fullName }}</h2>

  <h2>{{ count }}</h2>
  <button @click="increment">Incrementar</button>
  <button @click="decrease">Diminuir</button>
  <button @click="reset">Resetar</button>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      name: "Romim",
      lastname: "Carvalho",
      count: 0,
    };
  },
  computed: {
    fullName(): string {
      return `${this.name} ${this.lastname}`;
    },
  },
  methods: {
    increment() {
      this.count++;
    },
    decrease() {
      this.count--;
    },
    reset() {
      this.count = 0;
    },
  },
  watch: {
    //colocar a propriedade como si fosse um metodo
    count(newValue, oldValue) {
      console.log(oldValue);
      console.log(newValue);
    },
  },
});
</script>
