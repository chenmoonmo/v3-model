<template>
  <t-button @click="clickHandler"> 
    <template #default>123</template>
     </t-button>
  <test-component v-if="isShow" :name="name" />
</template>

<script setup>
import { ref, defineAsyncComponent } from "vue";
import TButton from "../components/TButton.vue";
const TestComponent = defineAsyncComponent(() =>
  import("../components/TestComponent.vue")
);
const isShow = ref(false);
const name = ref("");
const clickHandler = async () => {
  if (!isShow.value) {
    name.value = (await prompt("请输入姓名")) ?? "world";
  }
  isShow.value = !isShow.value;
};
</script>
