<template>
  <el-container class="layout-default">
    <el-header>
      <m-header />
    </el-header>
    <el-main>
      <nuxt/>
    </el-main>
    <el-footer>
      
    </el-footer>
  </el-container>
</template>

<script>
import MHeader from '@/components/header/index.vue'
export default {
  components: {
    MHeader
  }
}
</script>

<style>
</style>
