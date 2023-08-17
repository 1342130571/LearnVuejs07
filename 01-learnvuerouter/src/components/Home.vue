<template>
  <div>
    <h2>我是首页</h2>
    <p>我是首页内容，哈哈哈</p>

    <router-link to="/home/news">新闻</router-link>
    <router-link to="/home/message">消息</router-link>

    <router-view></router-view>

    <h2>{{message}}</h2>
  </div>
</template>

<script>
import router from "../router";

export default {
  name: 'Home',
  data() {
    return{
      message:'你好啊',
      path:'/home/news'
    }
  },
  // 生命周期函数
  // 组件被创建时
  created() {
  //   document.title = '首页'
    console.log('home created')
  },
//   组件结束时
//   destroyed() {
//     console.log('home destroyed');
//   },

  /*
  * activated 和 deactivated函数：
  *   这两个函数，只有该组件被保持了状态使用了keep-alive时，才是有效的
  * */

//   组件活跃时执行回调的函数
  activated() {
    // console.log(this.path);
    this.$router.push(this.path)
  },
//   组件不活跃时执行的回调函数
//   deactivated() {
//   }

//   离开之前调用的组件组件导航
  beforeRouteLeave(to ,from ,next) {
    console.log(this.$route.path);
    console.log(this.path);
    this.path = this.$route.path
    next()
  }
//   组件中的元素挂载至页面时
//   mounted() {
//     console.log('mounted');
//   },
// //   组件内容更新时
//   updated() {
//     console.log('updated');
//   }

}
</script>

<style>

</style>
