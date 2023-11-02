<template>
  <div class="h-[3000px] w-full bg-gradient-to-b from-red-100 to-yellow-100">
    My Page

    <div class="my-2">status: {{ status }}</div>

    <div class="flex items-center justify-center p-10">
      <button class="rounded bg-green-400 p-3" @click="openModal">Open</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { $emit, createPreset } from "vue-global-modal";

const status = ref("none");

const openModal = () => {
  $emit("MyModal", {
    onConfirm: () => {
      status.value = "Accepted";
    },
    onCancel: () => {
      status.value = "Rejected";
    },
  });
};
</script>
