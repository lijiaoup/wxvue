<template>
  <div class="home w-bgcolor">
    <van-swipe class="swiper"
      :autoplay="3000"
      indicator-color="red">
      <van-swipe-item class="relative"
        v-for="(image, index) in data.images"
        :key="index">
        <img :src="image" />
      </van-swipe-item>
    </van-swipe>
    <div class="flex-box">
      <div class="homeClassify"
        v-for="(d, index) in data.classlist"
        :key="index"
        @click="gotoSearch(d.id)">
        <div>
          <img :src="d.img" />
        </div>
        <p>{{d.name}}</p>
      </div>
    </div>
    <div class="homeSeckill">

    </div>
    <div class="homeActivities">
      <div class="homeTitle">
        <img src="@/assets/mrt1_7.png" />
      </div>
      <div class="flex-box typeOne">
          <div>1</div>
          <div>1</div>
          <div>1</div>
      </div>
      <div class="flex-box typeTwo">
        <div>1</div>
          <div>1</div>
          <div>1</div>
          <div>1</div>
          <div>1</div>
          <div>1</div>
      </div>
    </div>
    <div class="empty"></div>
    <Footer :active='0'></Footer>
  </div>
</template>

<script>
// @ is an alias to /src
import Footer from '@/components/Footer.vue';

export default {
  name: 'home',
  components: {
    Footer,
  },
  data() {
    return {
      active: 0,
      data: {
        images: [
          'https://img.yzcdn.cn/logo.png',
          'https://img.yzcdn.cn/2.jpg',
        ],
        classlist: [
          {
            id: '2029',
            img: 'http://filexiaoyuantest.jieletong.com/parameter/2019/04/1554704251761.png',
            name: '茶水饮料',
          },
          {
            id: '2029',
            img: 'http://filexiaoyuantest.jieletong.com/parameter/2019/04/1554704251761.png',
            name: '茶水饮料',
          },
          {
            id: '2029',
            img: 'http://filexiaoyuantest.jieletong.com/parameter/2019/04/1554704251761.png',
            name: '茶水饮料',
          },
          {
            id: '2029',
            img: 'http://filexiaoyuantest.jieletong.com/parameter/2019/04/1554704251761.png',
            name: '茶水饮料',
          },
          {
            id: '2029',
            img: 'http://filexiaoyuantest.jieletong.com/parameter/2019/04/1554704251761.png',
            name: '茶水饮料',
          },
          {
            id: '2029',
            img: 'http://filexiaoyuantest.jieletong.com/parameter/2019/04/1554704251761.png',
            name: '茶水饮料',
          },
          {
            id: '2029',
            img: 'http://filexiaoyuantest.jieletong.com/parameter/2019/04/1554704251761.png',
            name: '茶水饮料',
          },
          {
            id: '2029',
            img: 'http://filexiaoyuantest.jieletong.com/parameter/2019/04/1554704251761.png',
            name: '茶水饮料',
          },
          {
            id: '2029',
            img: 'http://filexiaoyuantest.jieletong.com/parameter/2019/04/1554704251761.png',
            name: '茶水饮料',
          },
          {
            id: '2029',
            img: 'http://filexiaoyuantest.jieletong.com/parameter/2019/04/1554704251761.png',
            name: '茶水饮料',
          },
        ],
      },

    };
  },
  methods: {

  },
};
</script>

<style lang="less">
.swiper {
  width: 16rem;
  height: 8rem;
  .relative {
    position: relative;
  }
  img {
    position: absolute;
    top: 50%;
    left: 50%;
    width: auto;
    height: auto;
    max-width: 16rem;
    max-height: 16rem;
    -webkit-transform: translate(-50%, -50%);
    -moz-transform: translate(-50%, -50%);
    -ms-transform: translate(-50%, -50%);
    -o-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
  }
}
.homeClassify {
  width: 20%;
  color: #454545;
  font-size: 0.58rem;
  > div {
    width: 80%;
    margin: 0 auto;
  }
}
.homeActivities {
  .homeTitle{
    border-bottom: 1px solid #f5f5f5;
  }
  .typeOne{
    > div {
      width: 50%;
      box-sizing: border-box;
      height: 4rem;
      border-bottom: 1px solid #f5f5f5;
      &:nth-child(2n+1){
    border-right: 1px solid #f5f5f5;
      }
    }
  }
  .typeTwo{
    border-top: 1px solid #f5f5f5;
    > div {
      width: 25%;
      box-sizing: border-box;
      height: 5rem;
      border-bottom: 1px solid #f5f5f5;
      border-right: 1px solid #f5f5f5;
      &:nth-child(4n){
      border-right:none;
      }
    }
  }
}
</style>
