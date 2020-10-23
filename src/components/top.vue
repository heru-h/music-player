<template>
  <div class="top-container">
    <div class="left-box">
      <div class="icon-wrapper">
        <img src='../assets/home.jpg' @click="$router.replace('/')" height="30" width="30">
      </div>
      <div class="history-wrapper">
        <span @click="$router.go(-1)" class="iconfont icon-arrow-lift"></span>
        <span @click="$router.go(1)" class="iconfont icon-arrow-right"></span>
      </div>
    </div>
    <div class ='mid-box'>
       <ul>
        <li>
          <router-link to="/discovery">
            <span class="el-icon-coffee"></span>
            发现音乐
          </router-link>
        </li>
        <li>
          <router-link to="/mvs">
            <span class="el-icon-ice-drink"></span>
            观看MV
          </router-link>
        </li>
        <li>
          <router-link to="/playlists">
            <span class="el-icon-ice-tea"></span>
            推荐歌单
          </router-link>
        </li>
        <li>
          <router-link to="/songs">
            <span class="el-icon-milk-tea"></span>
            最新音乐
          </router-link>
        </li>
      </ul>
    </div>
    <div class="right-box">
      <el-input size="small" @keyup.enter.native="toResult" placeholder="搜索" v-model.trim="query">
        <i slot="prefix" class="el-input__icon el-icon-search"></i>
      </el-input>
    </div>
  </div>
</template>

<script>
export default {
  name: "top",
  data() {
    return {
      query: "",
    };
  },
  methods: {
    toResult() {
      if (!this.query) {
        this.$message.warning("请输入查询内容");
      } else {
        this.$router.push(`/result?keywords=${this.query}`);
      }
    },
  },
};
</script>

<style lang="scss" scoped>
</style>
