<script setup>
  import dayjs from 'dayjs';
  import 'dayjs/locale/zh-cn';
  import locale from 'ant-design-vue/es/date-picker/locale/zh_CN';

  dayjs.locale('zh-cn');
</script>
<template>
  <a-config-provider :locale="locale">
    <div class="nav">
      <router-link to="/">首页</router-link>
      <router-link to="/about">关于</router-link>
    </div>
    <router-view />
  </a-config-provider>
</template>
<style lang="less" scoped>
  .nav {
    background-color: #515151;
    text-align: center;
    a {
      margin: 0 8px;
      color: #fff;
      &.router-link-active {
        color: rgb(163, 163, 255);
      }
    }
  }
</style>
