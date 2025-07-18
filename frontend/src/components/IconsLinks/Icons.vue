<template>
  <div class="icons">
    <a data-aos="fade-in" data-aos-duration="1400" data-aos-delay="600" href="#"><i class="ri-facebook-fill"></i></a>
    <a data-aos="fade-in" data-aos-duration="1400" data-aos-delay="700" href="#"><i class="ri-youtube-fill"></i></a>
    <a data-aos="fade-in" data-aos-duration="1400" data-aos-delay="800" href="#"><i class="ri-twitter-fill"></i></a>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
.icons {
  position: absolute;
  top: 50%;
  padding: 0 7%;
  transform: translateY(-50%);

  i {
    display: block;
    margin: 35px 0;
    color: var(--text-color);
    font-size: 23px;
    transition: all 0.6s;

    &:hover {
      transform: translateY(-5px);
      color: var(--main-color);
      margin-right: 6px;
    }
  }
}

@media (max-width: 1770px) {
  .icons {
    padding: 0 4%;
  }
}

@media (max-width: 1370px) {
  .icons {
    display: none;
  }
}
</style>
