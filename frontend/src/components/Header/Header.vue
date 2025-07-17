<template>
  <header class="header">
    <Logo />
    <NavList />
    <div class="right-content">
      <a href="#" class="nav-btn">Sign In</a>
      <div onclick="menuActive" class="bx bx-menu" id="menu-icon"></div>
    </div>
  </header>
</template>

<script setup lang="ts">
import Logo from '@/components/Header/Logo.vue'
import NavList from '@/components/Header/NavList.vue'
import { defineComponent } from 'vue'

export default defineComponent({
  setup() {
    function menuActive() {}

    return {
      menuActive,
    }
  },
})
</script>

<style scoped lang="scss">
@use '@/assets/styles/components/Header.scss';
</style>
