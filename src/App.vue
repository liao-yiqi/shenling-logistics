<script setup></script>

<template>
  <div id="app">
    <!-- <el-scrollbar ref="main" style="height: 100%; width: 100%">
    </el-scrollbar> -->
    <RouterView />
  </div>
</template>

<style scoped>
#app {
  /deep/ .el-scrollbar__wrap {
    overflow-x: hidden;
  }
}
</style>
