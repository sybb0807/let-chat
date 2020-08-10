<template>
  <el-menu
    class="bg-dark"
    style="height: 100%;"
    default-active="1"
    background-color="rgb(20, 20, 21)"
    active-text-color="#1296db"
  >
    <el-menu-item index="1" class="mt60">
      <el-avatar
        shape="square"
        :size="40"
        src="https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png"
      ></el-avatar>
    </el-menu-item>
    <el-menu-item index="1" class="mt20">
      <i class="f36 el-icon-message"></i>
    </el-menu-item>
    <el-menu-item index="2" class="mt10">
      <i class="f36 el-icon-menu"></i>
    </el-menu-item>
    <el-menu-item index="3" class="mt10">
      <i class="f36 el-icon-setting"></i>
    </el-menu-item>
  </el-menu>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class AsideNav extends Vue {}
</script>

<style scoped></style>
