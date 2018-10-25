<template>
  <el-container class="layout-default">
    <el-header>
      <m-header />
    </el-header>
    <el-main>
      <nuxt/>
    </el-main>
    <el-footer>Footer</el-footer>
  </el-container>
</template>

<script>
import MHeader from '@/components/public/header/index.vue'
export default {
  components: {
    MHeader
  }
}
</script>

<style>
</style>
