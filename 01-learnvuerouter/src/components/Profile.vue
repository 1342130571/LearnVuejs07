<script>
  export default {
    name:'Profile',
    // created() {
    //   document.title = '档案'
    // }
  }
</script>

<template>
<div>
  <h2>我是profile组件</h2>
  <h2>{{$route.query.name}}</h2>
  <h2>{{$route.query.age}}</h2>
  <h2>{{$route.query.height}}</h2>
</div>
</template>

<style scoped>

</style>
