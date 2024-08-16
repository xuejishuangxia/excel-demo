<template>
  <div id="container">
    <!-- <UniverSheet v-if="isShow" id="sheet" ref="univerRef" :data="data" /> -->
    <!-- <MySlot></MySlot> -->
    <AnimateCom></AnimateCom>
  </div>
</template>

<script setup lang="ts">
import { DEFAULT_WORKBOOK_DATA } from "./assets/default-workbook-data";
import { ref } from "vue";
// import UniverSheet from "./components/UniverSheet.vue";
// import MySlot from "./components/MySlot.vue";
import AnimateCom from "./components/AnimateCom.vue";

const data = ref(DEFAULT_WORKBOOK_DATA);
const univerRef = ref<InstanceType<typeof UniverSheet> | null>(null);
const isShow = ref(true);
</script>

<style scoped>
#container {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
}
#sheet {
  /** The height of the Union uses the height of the parent container */
  flex: 1;
}
</style>
