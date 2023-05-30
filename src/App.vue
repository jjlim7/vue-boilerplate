<template>
  <NavMenu></NavMenu>
  <el-container>
    <el-main>
      <router-view></router-view>
    </el-main>
  </el-container>
</template>

<script setup>
import {RouterView} from 'vue-router'
import NavMenu from './components/NavMenu.vue'
</script>