<template>
  <button v-on="attrs">
    <slot> click me </slot>
  </button>
</template>

<script setup>
import { defineEmit, useContext } from "vue";
const { attrs } = useContext();
// const emit = defineEmit(["click"]);
// const clickHandler = () => emit("click");
</script>

<style>
</style>