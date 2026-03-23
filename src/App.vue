// template : 节点中间用于放置 html 代码；
<!-- html 代码 -->
<template>
   <!-- 设置语言为中文 -->
   <el-config-provider :locale="locale">
      <div class="flex flex-col min-h-screen">
         <router-view></router-view>
      </div>
   </el-config-provider>
</template>

// script : 节点中间用于放置 javascript 代码；
<!-- js 代码, setup 标识通常和组合式 API 搭配使用, 用于告诉 Vue 需要在编译时进行一些处理，让我们可以更简洁地使用组合式 API -->
<script setup>
import zhCn from 'element-plus/dist/locale/zh-cn.mjs'
const locale = zhCn
console.log(import.meta.env)
</script>

// style : 节点中间用于放置 css 样式代码；
<!-- css 代码， scoped 表示节点内 css 样式只针对此组件有效，不影响其他组件 -->
<style scoped>
/* 自定义顶部加载 Loading 颜色 */
#nprogress .bar {
  background: #409eff!important;
}
/* 暗黑模式 body 背景色 */
.dark body {
   --tw-bg-opacity: 1;
    background-color: rgb(17 24 39 / var(--tw-bg-opacity));
}
</style>
