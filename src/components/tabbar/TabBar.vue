<template>
  <div id="tabbar">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'TabBar'
};
</script>

<style>
#tabbar{
  height: 59px;
  display: flex; /* 使用flex布局  */
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  font-size: 14px;
  background-color: #f6f6f6;
  box-shadow: 0 -1px 10px rgba(100, 100, 100, 0.3)

}
</style>