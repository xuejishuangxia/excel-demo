<template>
  <div class="animate-container">
    <button @click="show = !show">Toggle</button>
    <Transition
      name="custom-classes"
      enter-active-class="animate__animated animate__backInUp"
      leave-active-class="animate__animated animate__backOutDown"
    >
      <p v-if="show">hello</p>
    </Transition>
  </div>
</template>
<script lang="ts" setup>
import { ref } from "vue";
import 'animate.css';
const show = ref(true);
</script>
<style scoped>
/* .fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
} */
</style>
