<script>
export default {
  name: 'TabBarItem',
  props: {
    path: String,
    activeColor: {
      path: String,
      default: 'red'
    }
  },
  data() {
    return{
      // isActive: true
    }
  },
  computed: {
    isActive() {
      // indexOf()函数：
      //   == -1 时表示没有找到相同的数据 返回false
      //   ！== -1 时表示找到相同的数据 返回true
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle() {
      return this.isActive ? {color : this.activeColor} : {}
    }
  },
  methods: {
    itemClick() {
      // console.log('itemClick');
      this.$router.replace(this.path)
    }
  }
}
</script>

<template>
    <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isActive"><slot name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
    <div :style="activeStyle"><slot name="item-text"></slot></div>
    </div>
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
