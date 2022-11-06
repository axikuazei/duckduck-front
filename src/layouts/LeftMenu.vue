<template>
  <div v-for="item in menuItemList" :key="item.title">
    <menu-item v-bind="item"></menu-item>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import MenuItem from '../components/MenuItem.vue';

const menuItemList = ref([
  {
    title: 'bbbb',
    caption: 'caption1',
    link: 'https://bilibili.com',
    icon: '',
  },
  {
    title: '百度',
    caption: '百度',
    link: 'https://www.baidu.com',
    icon: '',
  },
  {
    title: '知乎',
    caption: '知乎',
    link: 'https://www.zhidu.com',
    icon: '',
  },
]);
</script>
<style lang="scss"></style>
