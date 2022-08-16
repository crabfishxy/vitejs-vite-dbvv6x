<script setup>
import { ref } from 'vue';
import {
  NConfigProvider,
  NInput,
  NDatePicker,
  NSpace,
  NButton,
} from 'naive-ui';

defineProps({
  msg: String,
  card: String,
  status: String,
});

const count = ref(0);
const todoInput = ref(null);

function addTodo() {
  console.log(todoInput.value);
}
</script>

<template>
  <h2>CrabFish's Todo</h2>
  <n-input-group>
    <n-input :style="{ width: '50%' }" ref="todoInput" />
    <n-button type="primary" @click="addTodo"> 添加 </n-button>
  </n-input-group>
</template>
