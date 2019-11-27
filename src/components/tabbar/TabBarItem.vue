<template>
  <div class="tabbar-item" @click="itemClick">
    <!-- <img src="" alt="">
    <div class="tabbar-item">首页</div>-->
    <div v-if="!isActive">
      <slot name="item-icon"></slot>
    </div>
    <div v-else>
      <slot name="item-icon-active"></slot>
    </div>
    <div :style="textColor">
      <slot name="item-text"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  computed:{
    isActive(){
      return this.$route.path.indexOf(this.path) !== -1
    },
    textColor(){
      return this.isActive ? {color: this.activeColor} : {}
    }
  },
  props: {
    path: String,
    activeColor: {
      type: String,
      default: 'red'
    }
  },
  methods: {
    itemClick() {
      if (this.$route.path != this.path) {
        this.$router.push(this.path);
      }    
    }
  }
};
</script>

<style>
.tabbar-item {
  flex: 1;
  text-align: center;
}
.tabbar-item img {
  width: 24px;
  height: 24px;
  margin-top: 3px;
  /* margin-bottom: -1px; */
  vertical-align: middle;
  margin-bottom: 2px;
}

</style>