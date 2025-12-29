<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<template>
  <RouterView />
</template>

<style lang="scss">
// 重置全局边距
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

// 确保 body 和 html 也没有额外间距
html,
body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}
</style>
