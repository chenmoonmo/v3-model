<template>
  {{ message }}
</template>

<script setup>
import { computed, defineProps } from "vue";
const props = defineProps({
  name: String,
});
const message = computed(() => `hello ${props.name}`);
</script>

<style>
</style>