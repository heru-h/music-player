<template>
  <div class="index-container">
 
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
