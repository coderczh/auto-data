<template>
  <div class="login-container">
    <div class="login">
      <el-form :model="loginForm" :rules="loginRules" label-width="auto">
        <div class="title">测试宝</div>
        <el-form-item label="账号：" prop="accountNo">
          <el-input
            v-model="loginForm.accountNo"
            placeholder="请输入帐号"
            style="width: 260px"
            size="large"
            clearable
          />
        </el-form-item>
        <br />
        <el-form-item label="密码：" prop="password">
          <el-input
            v-model="loginForm.password"
            type="password"
            placeholder="请输入密码"
            clearable
            show-password
            size="large"
          />
        </el-form-item>
        <br />
        <div style="text-align: center">
          <el-button
            size="large"
            type="primary"
            @click="onSubmit()"
            style="margin-right: 20px; width: 100px"
            >登录</el-button
          >
          <el-button size="large" style="width: 100px">注册</el-button>
        </div>
      </el-form>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { reactive } from 'vue'

const loginForm = reactive({
  accountNo: '',
  password: '',
})

const loginRules = reactive({
  accountNo: [
    {
      required: true,
      message: '请输入账号',
      trigger: 'blur',
    },
  ],
  password: [
    {
      required: true,
      message: '请输入密码',
      trigger: 'blur',
    },
  ],
})

const onSubmit = () => {}
</script>

<style lang="scss" scoped>
.login-container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
  background: url(@/static/image/login-bgd.svg);

  .login {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 500px;
    height: 350px;
    border: 1px solid #ccc;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);

    .title {
      font-size: 35px;
      text-align: center;
      margin-bottom: 30px;
      font-family: 'Microsoft YaHei', '微软雅黑', Arial, sans-serif;
      letter-spacing: 3px;
      font-weight: bold;
      color: #303030;
    }
  }
}

:deep(.el-form-item__label) {
  line-height: 40px;
  font-size: 15px;
}

:deep(.el-button--large) {
  font-size: 15px;
  line-height: 40px;
  letter-spacing: 3px;
}
</style>
