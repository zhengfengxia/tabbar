<template>
  <div id="app">
    <router-view></router-view>

    <tab-bar>
      <tab-bar-item path="/home" >
        <img slot="item-icon" src="./assets/img/tabbar/home.svg" alt />
        <img slot="item-icon-active" src="./assets/img/tabbar/home_active.svg" alt />
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category" activeColor='green'>
        <img slot="item-icon" src="./assets/img/tabbar/category.svg" alt />
        <img slot="item-icon-active" src="./assets/img/tabbar/category_active.svg" alt />
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/shop" activeColor='green'>
        <img slot="item-icon" src="./assets/img/tabbar/shop.svg" alt />
        <img slot="item-icon-active" src="./assets/img/tabbar/shop_active.svg" alt />
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile" activeColor='green'>
        <img slot="item-icon" src="./assets/img/tabbar/profile.svg" alt />
        <img slot="item-icon-active" src="./assets/img/tabbar/profile_active.svg" alt />
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
import TabBar from "./components/tabbar/TabBar";
import TabBarItem from "./components/tabbar/TabBarItem";
import route from 'vue-router'

export default {
  name: "App",
  components: {
    TabBar,
    TabBarItem
  }
};
</script>

<style>
/* 引入css文件 */
@import "./assets/css/reset.css";
</style>
