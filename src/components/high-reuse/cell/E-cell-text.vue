<template>
  <div class="E-cell-text">
    <van-cell title="配置文件" value="点击编辑" size="20px" @click="show=true" />
    <van-popup v-model="show">
      <E-config-json v-if="show" @close="show=false" />
    </van-popup>
  </div>
</template>

<script>
import EConfigJson from "@/components/high-reuse/cell/E-config-json";
export default {
  components: { EConfigJson },
  data() {
    return {
      show: false
    };
  }
};
</script>