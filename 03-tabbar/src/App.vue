<template>
  <div id="app">
    <tab-bar>
      <tab-bar-item path="/home" activeColor="deeppink">
<!--        <img src="../../assets/img/tabbar/shouye.png" alt="">-->
<!--        <div>首页</div>-->
        <img slot="item-icon" src="./assets/img/tabbar/shouye.png" alt="">
        <img slot="item-icon-active" src="./assets/img/tabbar/shouyexuanzhong.png" alt="">
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category" activeColor="deeppink">
        <img slot="item-icon" src="./assets/img/tabbar/fenlei.png" alt="">
        <img slot="item-icon-active" src="./assets/img/tabbar/fenleixuanzhong.png" alt="">
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/cart" activeColor="deeppink">
        <img slot="item-icon" src="./assets/img/tabbar/gouwuche.png" alt="">
        <img slot="item-icon-active" src="./assets/img/tabbar/gouwuchexuanzhong.png" alt="">
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile" activeColor="deeppink">
        <img slot="item-icon" src="./assets/img/tabbar/wode.png" alt="">
        <img slot="item-icon-active" src="./assets/img/tabbar/wodexuanzhong.png" alt="">
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-bar>
    <router-view></router-view>
  </div>
</template>

<script>
import TabBar from "./components/tabbar/TabBar.vue";
import TabBarItem from "./components/tabbar/TabBarItem.vue";
export default {
  name: 'App',
  components: {
    TabBar,
    TabBarItem
  }
}
</script>

<style>
  @import "./assets/css/base.css";
</style>
