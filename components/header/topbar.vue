<template>
  <el-row
    :gutter="20"
    class="m-header">
    <el-col :span="6">
      <geo />
    </el-col>
    <el-col :span="6">
      <user />
    </el-col>
    <el-col :span="12">
      <navbar />
    </el-col>
  </el-row>
</template>

<script>
import Geo from './geo.vue'
import Navbar from './nav.vue'
import User from './user.vue'

export default {
  components: {
    Geo,
    Navbar,
    User
  }
}
</script>

<style lang="scss">
</style>
