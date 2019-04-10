<template>
  <div class="hello">
    <van-tabbar v-model="activeindex"
      active-color="#ff0000">
      <van-tabbar-item icon="wap-home"
        @click="goTo(0)">首页</van-tabbar-item>
      <van-tabbar-item icon="apps-o"
        @click="goTo(1)">分类</van-tabbar-item>
      <van-tabbar-item icon="description"
        @click="goTo(0)">资讯</van-tabbar-item>
      <van-tabbar-item icon="cart-o"
        info="5"
        @click="goTo(0)">购物车</van-tabbar-item>
      <van-tabbar-item icon="manager-o"
        @click="goTo(0)">我</van-tabbar-item>
    </van-tabbar>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    active: Number,
  },
  data() {
    return {
      activeindex: this.active
    }
  },
  methods: {
    goTo(flag) {
      const that = this;
      switch (flag) {
        case 0:
          that.$router.push({
            path: '/',
          });
          break;
        case 1:
          that.$router.push({
            path: '/user',
          });
          break;
        case 2:
          that.$router.push({
            path: '/apply',
          });
          break;
        case 3:
          that.$router.push({
            path: '/consulting',
          });
          break;
        case 4:
          that.$router.push({
            path: '/partymembe',
            query: {
              type: '1',
            },
          });
          break;
        default:
          break;
      }
    },
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">

</style>
