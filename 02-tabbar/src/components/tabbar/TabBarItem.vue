<script>
export default {
  name: 'TabBarItem'
}
</script>

<template>
  <div class="tab-bar-item">
    <slot name="item-icon"></slot>
    <slot name="item-text"></slot>
<!--    <img src="../../assets/img/tabbar/shouye.png" alt="">
    <div>首页</div>-->
  </div>
<!--  <div class="tab-bar-item">-->
<!--    <img src="../../assets/img/tabbar/fenlei.png" alt="">-->
<!--    分类-->
<!--  </div>-->
<!--  <div class="tab-bar-item">-->
<!--    <img src="../../assets/img/tabbar/gouwuche.png" alt="">-->
<!--    购物车-->
<!--  </div>-->
<!--  <div class="tab-bar-item">-->
<!--    <img src="../../assets/img/tabbar/wode.png" alt="">-->
<!--    我的-->
<!--  </div>-->
</template>

<style scoped>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}

.tab-bar-item img {
  width: 24px;
  height: 24px;
  margin-top: 3px;
  vertical-align: middle;
  margin-bottom: 2px;
}
</style>
