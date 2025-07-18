<template>
  <section class="hero">
    <div class="hero-text">
      <h5 data-aos="fade-right" data-aos-duration="1400">#Coffee for hot days</h5>
      <h1 data-aos="zoom-in-left" data-aos-duration="1400" data-aos-delay="200">- Cold Brew</h1>
      <p data-aos="fade-right" data-aos-duration="1400" data-aos-delay="300">
        Boots your productivity and build your mood with a glass of coffee in the morning. Coffee
        has a stimulating effect.
      </p>
      <div data-aos="flip-down" data-aos-duration="1400" data-aos-delay="400" class="main-hero">
        <a href="#" class="btn">Order Now</a>
        <a href="#" class="price">$16.00 | <span>Regular Price</span></a>
      </div>
    </div>
    <div data-aos="zoom-in" data-aos-duration="1400" class="hero-img">
      <img src="@/assets/images/hero.png" />
    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.hero {
  padding: 0 14%;
  position: relative;
  width: 100%;
  height: 100vh;
  background-size: cover;
  background: url(@/assets/images/bg.png) center;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  align-items: center;
  gap: 2rem;

  .hero-img img {
    width: 100%;
    height: auto;
  }

  .hero-text {
    h1 {
      font-size: var(--big-font);
      font-weight: 900;
      margin: 15px 0;
    }

    h5 {
      font-size: 18px;
      font-weight: 400;
      letter-spacing: 1px;
    }

    p {
      width: 100%;
      max-width: 620px;
      font-size: var(--p-font);
      font-weight: 400;
      line-height: 32px;
      color: var(--text-color);
      margin-bottom: 40px;
    }

    .main-hero {
      display: flex;
      align-items: center;

      .btn {
        display: inline-block;
        padding: 13px 32px;
        background: var(--main-color);
        border: 2px solid transparent;
        border-radius: 7px;
        color: var(--text-color);
        font-weight: 500;
        transition: all 0.6s ease;
        margin-right: 20px;

        &:hover {
          transform: scale(1.1);
        }
      }

      .price {
        display: flex;
        align-items: center;
        font-size: 28px;
        font-weight: bold;
        color: var(--text-color);

        span {
          font-size: 17px;
          font-weight: 400;
          color: var(--main-color);
          margin-left: 10px;
        }
      }
    }
  }
}

@media (max-width: 1370px) {
  .hero {
    padding: 0 4%;

    .price {
      font-size: 20px;
    }

    .btn {
      padding: 10px 23px;
    }
  }
}

@media (max-width: 920px) {
  .hero {
    grid-template-columns: 1fr;
    height: auto;

    .hero-text {
      padding-top: 130px;
    }

    .hero-img {
      height: 500px;
      width: 500px;
      margin: 0 auto;

      img {
        width: 100%;
        height: 100%;
        object-fit: contain;
      }
    }
  }
}

@media (max-width: 570px) {
  .hero {
    height: 100vh;

    .hero-img {
      height: 400px;
      width: 400px;
      margin: 0 auto;
    }
  }
}
</style>
