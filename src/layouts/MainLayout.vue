<template>
  <q-layout view="hHr lpR fff">
    <q-header reveal elevated class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="toggleLeftDrawer" />

        <q-toolbar-title> 丫丫 </q-toolbar-title>

        <q-btn dense flat round icon="menu" @click="toggleRightDrawer" />
      </q-toolbar>
      <navi-tab></navi-tab>
    </q-header>

    <q-drawer
      show-if-above
      v-model="leftDrawerOpen"
      side="left"
      bordered
      :width="150"
    >
      <left-menu></left-menu>
    </q-drawer>

    <q-drawer
      show-if-above
      v-model="rightDrawerOpen"
      side="right"
      bordered
      :width="150"
    >
      <!-- drawer content -->
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

    <footer-layout></footer-layout>
  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import NaviTab from './NaviTab.vue';
import LeftMenu from './LeftMenu.vue';
import FooterLayout from './FooterLayout.vue';

const leftDrawerOpen = ref(false);
const rightDrawerOpen = ref(false);
function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
function toggleRightDrawer() {
  rightDrawerOpen.value = !rightDrawerOpen.value;
}
</script>
<style lang="scss"></style>
FooterLayout
