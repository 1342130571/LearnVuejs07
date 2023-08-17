<script>
  export default {
    name: 'TabBar'
  }
</script>

<template>
  <div id="tab-bar">
    <slot></slot>
  </div>
</template>

<style scoped>
#tab-bar {
  display: flex;
  background-color: #f6f6f6;

  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;

  /*
    box-shadow：用于在元素的框架上添加阴影效果
      x偏移量 ， y偏移量 ， 阴影模糊半径 ， 颜色
  */
  box-shadow: 0 -1px 1px rgba(100,100,100,0.2)
}
</style>
