<script setup>
import { ref } from "vue";
import ChildComponent from "./ChildComponent.vue";
const message = "This message from Parent component!"
const messageFromChild = ref("");

</script>

<template>
  <div class="w-[850px] p-3 rounded-3xl bg-gradient-to-r from-pink-500/70 via-red-500/70 to-yellow-500/70">
    <div class="p-10 bg-white back rounded-3xl">
      <h2 class="mb-5 text-4xl font-semibold">Parrent Component</h2>
      <h1 class="mb-5 text-lg font-bold">Emit message from Child component: <span class="text-green-500">{{ messageFromChild }}</span></h1>
      <ChildComponent :message="message" v-model:messageFromChild="messageFromChild" />
    </div>
  </div>
</template>

<style scoped></style>