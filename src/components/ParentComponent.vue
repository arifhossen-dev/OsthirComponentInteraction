<script setup>
import { ref } from "vue";
import ChildComponent from "./ChildComponent.vue";
const props = defineProps(["message"]);
const messageFromChild = ref("");

</script>

<template>
  <div class="p-10 border-8 rounded-3xl border-black/50 w-[650px]">
    <h2 class="mb-5 text-4xl font-semibold">Parrent Component</h2>
    <h1 class="mb-5 text-lg font-bold">{{ messageFromChild }}</h1>
    <ChildComponent :message="props.message" v-model:messageFromChild="messageFromChild" />
  </div>
</template>

<style scoped></style>