<template>
  <lay-button @click="changeVisible">开始</lay-button>
  <br/>
  <br/>
  <lay-transition>
    <lay-card title="标题" v-if="visible">内容</lay-card>
  </lay-transition>
</template>

<script setup>
import { ref } from "vue";

const visible = ref(true);

const changeVisible = () => {
    visible.value = !visible.value;
}
</script>
