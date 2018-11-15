<template>
  <div class="search-panel">
    <el-row class="m-header-searchbar">
      <el-col
        :span="4"
        class="left">
        <img
          src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/logo.png"
          alt="美团">
      </el-col>
      <el-col
        :span="14"
        class="center">
        <div class="wrapper">
          <el-input
            v-model="search"
            placeholder="搜索商家或地点"
            @focus="focus"
            @blur="blur"
          />
          <button class="el-button el-button-primary">
            <i class="el-icon-search" />
          </button>
          <dl
            v-if="isHotPlace"
            class="hotPlace">
            <dt>热门推荐</dt>
            <dd
              v-for="(item, idx) in hotPlaceList"
              :key="idx">{{ item }}</dd>
          </dl>
          <dl
            v-if="isSearchList"
            class="searchList">
            <dd
              v-for="(item, idx) in searchList"
              :key="idx">{{ item }}</dd>
          </dl>
        </div>
        <p class="suggest">
          <a href="">故宫博物院</a>
          <a href="">故宫博物院</a>
          <a href="">故宫博物院</a>
          <a href="">故宫博物院</a>
          <a href="">故宫博物院</a>
        </p>
        <ul class="nav">
          <li>
            <nuxt-link
              to="/"
              class="movie">猫眼电影</nuxt-link>
            <nuxt-link
              to="/"
              class="hotel">美团酒店</nuxt-link>
            <nuxt-link
              to="/"
              class="apaetment">民宿/公寓</nuxt-link>
            <nuxt-link
              to="/"
              class="business">商家入驻</nuxt-link>
          </li>
        </ul>
      </el-col>
      <el-col
        :span="6"
        class="right">
        <ul class="security">
          <li>
            <i class="refund">
              <p class="txt">随时退</p>
            </i>
          </li>
          <li>
            <i class="single">
              <p class="txt">不满意免单</p>
            </i>
          </li>
          <li>
            <i class="overdue">
              <p class="txt">过期退</p>
            </i>
          </li>
        </ul>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: '',
      isFocus: false,
      hotPlaceList: ['故宫', '圆明园', '长城'],
      searchList: ['故宫', '鸟巢', '香山']
    }
  },
  computed: {
    isHotPlace() {
      return this.isFocus && !this.search
    },
    isSearchList() {
      return this.isFocus && this.search
    }
  },
  methods: {
    focus() {
      this.isFocus = true
    },
    blur() {
      setTimeout(() => {
        this.isFocus = false
      }, 300)
    },
    input() {
      console.log('input')
    }
  }
}
</script>

<style lang="scss" scoped>
</style>
