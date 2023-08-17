<template>
  <div id="app">
    <h2>我是APP组件</h2>
<!--    <router-link to="/home" tag="button" replace active-class="active">首页</router-link>-->
<!--    <router-link to="/about" tag="button" replace active-class="active">关于</router-link>-->

<!--    <router-link to="/home" tag="button" replace>首页</router-link>-->
<!--    <router-link to="/about" tag="button">关于</router-link>-->

<!--    <button @click="homeClick">首页</button>-->
<!--    <button @click="aboutClick">关于</button>-->

    <router-link to="/home" tag="button">首页</router-link>
    <router-link to="/about" tag="button">关于</router-link>
<!--    <router-link :to="'/user/'+userId" tag="button">用户</router-link>-->
<!--&lt;!&ndash;    <router-link to="/profile" tag="button">档案</router-link>&ndash;&gt;-->
<!--    <router-link :to="{path: '/profile' , query:{name:'why' , age:18, height: 1.88}}" tag="button">档案</router-link>-->

    <button @click="clickUserid">用户</button>
    <button @click="clickProfile">档案</button>

<!--    keep-alive：
          include -- 字符串或正则表达式，只有匹配的组件会被缓存
          exclude -- 字符串或正则表达式，任何匹配的组件都不会被缓存-->

    <keep-alive exclude="Profile,User">
      <router-view></router-view>
    </keep-alive>


  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return{
      userId:'Lisi'
    }
  },
  methods:{
    homeClick() {
      //通过代码的方式修改路由 vue-router
      //push => pushState
      // this.$router.push('/home')
      this.$router.replace('/home')
      console.log('homeClick');
    },
    aboutClick() {
      // this.$router.push('/about')
      this.$router.replace('/about')
      console.log('aboutClick');
    },
    clickUserid() {
      this.$router.push('/user/'+this.userId)
      console.log('user');
    },
    clickProfile() {
      this.$router.push({
        path:'/profile',
        query:{
          name:'kobe',
          age:18,
          height:1.88
        }
      })
      console.log('profile');
    }
  }
}
</script>

<style>
  /*.router-link-active{
    color: #f00;
  }*/

  .active{
    color: #f00;
  }
</style>
