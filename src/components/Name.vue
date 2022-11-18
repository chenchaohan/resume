<template>
  <div class="flex flex-col sm:flex-row justify-between">
    <div class="flex flex-col justify-center">
      <span class="text-2xl font-medium mb-2">陈超汉</span>
      <div>
        <label class="inline-block w-18 sm:hidden">博客:</label>
        <a href="https://www.ebxcom.cn" target="_blank">https://www.ebxcom.cn</a>
      </div>
    </div>
    <div>
      <div>
        <label class="inline-block w-18">Github:</label>
        <a href="https://github.com/chenchaohan" target="_blank">
          https://github.com/chenchaohan
        </a>
      </div>
      <div>
        <label class="inline-block w-18">电子邮件:</label>
        <a href="mailto:chenchaohan@live.com"> chenchaohan@live.com </a>
      </div>
      <div v-if="phone">
        <label class="inline-block w-18">手机号码:</label>
        {{ phone }}
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { onMounted, ref } from "vue";

const phone = ref<string | null>(null);

// localStorage.setItem("phone", "18082962808");

onMounted(() => {
  phone.value =localStorage.getItem("phone")||"18082962808";
});
</script>
