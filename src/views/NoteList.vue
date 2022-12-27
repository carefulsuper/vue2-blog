<template>
  <div>
    <el-breadcrumb separator="/">
      <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
      <el-breadcrumb-item :to="{ path: '/note' }">技术选型</el-breadcrumb-item>
      <el-breadcrumb-item :to="{ path: '/about' }">活动列表</el-breadcrumb-item>
      <el-breadcrumb-item :to="{ path: '/detail' }">活动详情</el-breadcrumb-item>
      <el-breadcrumb-item :to="{ path: '/detail' }">活动详情</el-breadcrumb-item>
    </el-breadcrumb>
    这是笔记列表
  </div>
</template>

<script>
    export default {
        name: "NoteList"
    }
</script>

<style scoped>

</style>
