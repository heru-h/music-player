<template>
  <div class="index-container">
    <div class="nav">
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
    <div class="main">
      <router-view></router-view>
    </div>
    <div class="player">
      <audio controls autoplay :src="url" loop></audio>
    </div>
  </div>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      activeIndex: 0,
      url: "",
    };
  },
};
</script>

<style lang="scss">
</style>
