<template>
  <div id="app">
    <div class="header mt40 clearfix">
      <!-- 使用 router-link 组件来导航. -->
      <!-- 通过传入 `to` 属性指定链接. -->
      <!-- <router-link> 默认会被渲染成一个 `<a>` 标签 -->
      <router-link to="/" v-bind:class="{active: isActive}" v-on:click="doSomething">Go to Hello</router-link>
      <br>
      <router-link to="/about" v-bind:class="{active: !isActive}" v-on:click="doSomething">Go to About</router-link>
    </div>
    <router-view></router-view>
  </div>
</template>

<script type="text/javascript">
export default {
  name: 'home',
  data(){
    return {
      isActive: true
    }
  },
  methods: {
    doSomething: function(){
      this.isActive = !this.isActive;
    }
  }
};
</script>

<style>
@import "./css/index.css";
</style>
