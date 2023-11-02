<template>
  <GlobalModal
    name="MyModal"
    class="fixed left-0 top-0 h-0 w-0 transition-all"
    v-slot="{ onConfirm, onCancel }"
    classOnShow="opacity-100"
    classOnHide="opacity-0 pointer-events-none"
    :showLogs="true"
  >
    <div
      class="absolute flex h-screen w-screen items-center justify-center bg-black/50"
    >
      <div
        class="flex h-full max-h-40 w-full max-w-sm flex-col rounded-lg bg-white p-5"
      >
        <div class="flex flex-1 font-bold">Modal</div>

        <div class="flex justify-end gap-2">
          <button
            class="rounded bg-gray-100 px-5 py-2 transition-all hover:brightness-95 active:scale-95"
            @click="onCancel"
          >
            Cancel
          </button>
          <button
            class="rounded bg-blue-500 px-5 py-2 font-bold text-white transition-all hover:brightness-105 active:scale-95"
            @click="onConfirm"
          >
            Okay
          </button>
        </div>
      </div>
    </div>
  </GlobalModal>
</template>

<script setup>
import GlobalModal from "vue-global-modal";
</script>
