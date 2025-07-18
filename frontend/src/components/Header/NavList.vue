<template>
  <ul class="nav_list" :class="{ open: isActive }">
    <li v-for="item in listItems" :key="item.text" class="nav_list_item">
      <a :href="item.link">{{ item.text }}</a>
    </li>
  </ul>
</template>

<script setup>
defineProps({
  isActive: {
    type: Boolean,
    default: false,
  }
})

const listItems = [
  { text: 'About', link: '#' },
  { text: 'Membership', link: '#' },
  { text: 'Events', link: '#' },
  { text: 'Contact', link: '#' }
]
</script>


<style lang="scss">
.nav_list {
  display: flex;

  a {
    display: inline-block;
    margin: 0 35px;
    color: var(--text-color);
    font-size: var(--p-font);
    transition: all 0.5s ease;

    &:hover {
      color: var(--main-color);
    }
  }
}

@media (max-width: 950px) {
  .nav_list {
    position: absolute;
    width: 100%;
    height: 100vh;
    padding: 100px 50px;
    top: 0;
    right: 0;
    bottom: 0;
    left: 100%;
    display: flex;
    flex-direction: column;
    backdrop-filter: blur(32px);
    transition: all 0.6s ease-in-out;

    a {
      display: block;
      padding: 0;
      margin: 0px 0px 25px 0px;
      font-size: 1.7rem;
    }
  }

  .nav_list.open {
    left: 0;
  }
}
</style>
