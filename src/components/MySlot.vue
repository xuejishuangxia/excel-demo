<template>
  <DefineSlotCom>
    <template v-slot:header>
      <el-row :gutter="20">
          <el-col :span="12">
            <div class="detail-text">
              <div class="text-title">编码：</div>
              <div class="text-value">code</div>
            </div>
          </el-col>
          <el-col :span="12">
            <div class="detail-text">
              <div class="text-title">名称：</div>
              <div class="text-value">名称</div>
            </div>
          </el-col>
        </el-row>
    </template>
    <template v-slot:main>
      <p>自定义的主要内容。</p>
    </template>
    <template v-slot:footer>
      <p>自定义的尾部。</p>
    </template>
    <template v-slot="{ slotProps }">
        <p>{{ slotProps.name }} - {{ slotProps.price }}元</p>
      </template>
  </DefineSlotCom>
</template>
<script lang="ts" setup>
import DefineSlotCom from "./DefineSlotCom.vue";
</script>
<style scoped></style>
