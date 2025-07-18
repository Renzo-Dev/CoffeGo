<template>
  <header class="header">
    <Logo />
    <NavList :isActive="showNavList" />
    <div class="right-content">
      <a href="#" class="nav-btn">Sign In</a>
      <div
        @click.prevent="toggleMenu"
        :class="['bx', showNavList ? 'bx-x' : 'bx-menu']"
        id="menu-icon"
      ></div>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import Logo from '@/components/Header/Logo.vue'
import NavList from '@/components/Header/NavList.vue'

const showNavList = ref(false)

const toggleMenu = () => {
  showNavList.value = !showNavList.value
}
</script>

<style scoped lang="scss">
@use '@/assets/styles/components/Header.scss';
</style>

<style scoped lang="scss">
@use '@/assets/styles/components/Header.scss';
</style>
