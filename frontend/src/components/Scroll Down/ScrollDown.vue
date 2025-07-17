<template>
  <div class="scroll">
    <a href="#">
      <i class="ri-scroll-to-bottom-line"></i>
      Scroll Down
    </a>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.scroll {
  position: absolute;
  top: 92%;
  right: 7%;
  transform: translateY(-50%);

  a {
    font-size: 16px;
    color: var(--text-color);

    i {
      font-size: 20px;
      color: var(--text-color);
      margin-right: 6px;
    }
  }
}

@media (max-width: 1770px) {
  .scroll {
    right: 4%;
  }
}

@media (max-width: 920px) {
  .scroll {
    display: none;
  }
}
</style>
