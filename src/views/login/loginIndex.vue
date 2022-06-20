<template>
  <div class="login-container">
    <el-form ref="formRef" :model="form" class="login-form">
      <div class="title-container">
        <h3 class="title">用户登录</h3>
      </div>
      <el-form-item>
        <el-icon :size="20" class="svg-container">
          <Edit />
        </el-icon>
        <el-input v-model="form.name" />
      </el-form-item>
      <el-form-item>
        <el-icon :size="20" class="svg-container">
          <Edit />
        </el-icon>
        <el-input v-model="form.password" />
      </el-form-item>
       <el-button type="primary" class="login-button">登录</el-button>
    </el-form>
  </div>
</template>
<script setup>
import { ref } from 'vue'
import { Edit } from '@element-plus/icons-vue'
const form = ref({
  name: '',
  password: ''
})
</script>
<style lang="scss" scoped>
.login-container {
  min-height: 100%;
  width: 100%;
  background-color: #2d3a4b;
  overflow: hidden;
  .login-form {
    position: relative;
    width: 520px;
    max-width: 100%;
    padding: 160px 35px 0;
    margin: 0 auto;
    overflow: hidden;
    ::v-deep .el-form-item {
      border: 1px solid rgba(255, 255, 255, 0.1);
      background: rgba(0, 0, 0, 0.1);
      border-radius: 5px;
      color: #454545;
    }
    ::v-deep .el-input {
      display: inline-block;
      height: 47px;
      width: 85%;

      input {
        background: transparent;
        border: 0px;
        -webkit-appearance: none;
        border-radius: 0px;
        padding: 12px 5px 12px 15px;
        color: #eee;
        height: 47px;
        caret-color: #fff;
      }
    }
    .login-button {
      width: 100%;
      box-sizing: border-box;
    }
  }
}

.svg-container {
  padding: 6px 5px 6px 15px;
  color: #889aa4;
  vertical-align: middle;
  display: inline-block;
}

.title-container {
  position: relative;
  .title {
    font-size: 26px;
    color: #eee;
    margin: 0px auto 40px auto;
    text-align: center;
    font-weight: bold;
  }
}
</style>
