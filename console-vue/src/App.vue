<template>
  <div id="app">
    <el-menu theme="dark" :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
      <el-menu-item index="1">全部资源</el-menu-item>
      <el-menu-item index="5">项目</el-menu-item>
      <el-menu-item index="3">应用</el-menu-item>
      <el-menu-item index="4">文档</el-menu-item>
      <el-menu-item index="6">模型</el-menu-item>
      <el-menu-item index="7">数据集</el-menu-item>
      <el-submenu index="2">
        <template slot="title">视图</template>
        <el-menu-item index="2-3">应用</el-menu-item>
        <el-menu-item index="2-3">报表</el-menu-item>
        <el-menu-item index="2-3">页面</el-menu-item>
      </el-submenu>
    </el-menu>
    <el-breadcrumb separator="/">
      <el-breadcrumb-item :to="{ path: '/' }">资源</el-breadcrumb-item>
      <el-breadcrumb-item>活动管理</el-breadcrumb-item>
    </el-breadcrumb>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      activeIndex: '1'
    }
  },
  methods: {
    handleSelect (key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>

<style>
body {
  margin: 0;
  background-color: #F9FAFC;
}

.el-menu {
  border-radius: 0;
}

.el-breadcrumb {
  padding: 15px;
}
</style>
