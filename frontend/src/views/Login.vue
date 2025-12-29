<template>
  <div class="login-container">
    <div class="login">111</div>
  </div>
</template>

<script lang="ts" setup></script>

<style lang="scss" scoped>
.login-container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
  background: url(@/static/image/login-bgd.svg);

  .login {
    width: 500px;
    height: 500px;
    border: 1px solid #ccc;
  }
}
</style>
