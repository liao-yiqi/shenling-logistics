<script setup lang="ts">
const loginForm = {
  account: '',
  password: '',
  code: ''
}
</script>

<template>
  <div class="login-container">
    <div class="shadow"></div>
    <video
      src="../../assets/video.mp4"
      loop
      muted
      autoplay
      style="width: 100%; height: 100%; object-fit: fill"
    />
    <el-form
      ref="loginForm"
      :model="loginForm"
      autocomplete="off"
      label-position="left"
      class="login-form"
    >
      <div class="title-container">
        <img src="../../assets/logo1.png" />
      </div>
      <el-form-item prop="account">
        <el-input
          ref="account"
          v-model="loginForm.account"
          placeholder="账号"
          autocomplete="off"
          name="account"
          type="text"
        />
        <img src="../../assets/icon-account.png" class="icon-img" />
      </el-form-item>
      <el-form-item prop="password">
        <el-input
          ref="password"
          v-model="loginForm.password"
          placeholder="密码"
          :show-password="true"
          autocomplete="off"
          name="password"
          type="password"
        />
        <img src="../../assets/icon-password.png" class="icon-img" />
      </el-form-item>
      <el-form-item class="code-input" prop="code">
        <el-input
          ref="code"
          v-model="loginForm.code"
          placeholder="验证码"
          autocomplete="off"
          name="code"
          style="width: 100%"
          type="text"
        />
        <img src="../../assets/icon-code.png" class="icon-img" />
      </el-form-item>
      <el-button class="login-button" type="primary">登录</el-button>
    </el-form>
  </div>
</template>

<style lang="scss" scoped>
$bg: #283443;
$light_gray: #fff;
$cursor: #555;

.login-container {
  .el-input {
    display: inline-block;
    input {
      background: transparent;
      border: 0;
      border-radius: 5px;
      color: #000000;
      caret-color: $cursor;

      &:-webkit-autofill {
        box-shadow: 0 0 0 1000px $bg inset !important;
        -webkit-text-fill-color: $cursor !important;
      }
    }
  }

  :deep(.el-input--prefix .el-input__inner) {
    padding-left: 48px;
    line-height: 54px;
    height: 54px;
    border-radius: 5px;
  }

  :deep(.el-input__icon) {
    line-height: 54px;
    font-size: 20px;
    padding-left: 12px;
    padding-right: 26px;
  }

  :deep(.el-form-item__content) {
    position: relative;
    .icon-img {
      width: 21px;
      height: 21px;
      position: absolute;
      left: 14px;
      top: 14px;
    }
    .el-input__inner {
      padding-left: 36px;
      height: 50px;
    }
  }

  :deep(.el-form-item) {
    border-radius: 5px;
    color: #454545;
    transition: all 0.3s;
    &:hover {
      border-color: #000408;
    }
  }
  :deep(.el-input__wrapper) {
    width: 100%;
  }
}
.login-button {
  width: 100%;
  height: 54px;
  margin-bottom: 14px;
  margin-top: 22px;
  background-color: #e15536;
  border: 0px;
  font-size: 18px;
  color: white;
  font-weight: bold;
}
</style>

<style lang="scss" scoped>
.login-container {
  background-size: 100% 100%;
  height: 100vh;
  overflow: hidden;
  position: relative;
  .shadow {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0.3;
    background: #1a1c41;
  }
  .login-form {
    border-radius: 10px;
    position: absolute;
    top: 45%;
    left: 45%;
    background: #fff;
    margin: -180px 0 0 -160px;
    width: 450px;
    height: 467px;
    padding: 36px 40px;
  }
  .title-container {
    position: relative;
    margin-bottom: 28px;
    text-align: center;
    img {
      height: 54px;
    }
  }
}
</style>
