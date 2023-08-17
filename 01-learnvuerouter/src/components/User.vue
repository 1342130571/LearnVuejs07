<script>
  export default {
    name:"User",
    computed:{
      userId() {
        return this.$route.params.userId
      }
    },
    // created() {
    //   document.title = '用户'
    // },
    methods:{
      // 所有的组件对象都继承自Vue类的原型
    }
  }
</script>

<template>
  <div>
    <h2>我是用户界面</h2>
    <p>我是用户界面的相关信息，嘿嘿嘿</p>
    <h2>{{userId}}</h2>
  </div>
</template>

<style scoped>

</style>
