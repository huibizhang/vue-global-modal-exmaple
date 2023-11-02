<script setup>
import MyModal from "./components/MyModal.vue";
import MyPage from "./components/MyPage.vue";
</script>

<template>
  <div class="flex h-screen w-screen flex-col">
    <div
      class="flex h-20 w-full items-center bg-blue-500 p-5 text-2xl font-bold text-white"
    >
      Header
    </div>

    <div class="flex w-full flex-1 overflow-y-auto p-5">
      <MyPage />
    </div>
  </div>
  <MyModal />
</template>
