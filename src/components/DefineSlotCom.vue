<template>
  <div class="child-component">
    <header>
      <slot name="header">默认头部</slot>
    </header>
    <main>
      <slot name="main">默认主要内容</slot>
    </main>
    <footer>
      <slot name="footer">默认尾部</slot>
    </footer>
    <slot :slotProps="item">
      默认内容：{{ item.name }}
    </slot>
  </div>
</template>
<script lang="ts" setup>
const item = { name: "卡皮巴拉",price:100 };
</script>
<style scoped></style>
