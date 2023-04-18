<template>
  <div class="flex-wrapper">
    <section class="gallery-container">
      <div class="gallery-image rot"></div>
      <div class="gallery-image hochzeitsmesse"></div>
      <div class="gallery-image grün"></div>
      <div class="gallery-image gruppe-grid"></div>
      <div class="gallery-image blau"></div>
    </section>
  </div>
</template>

<script>
import "../assets/stylesheets/global.scss";
export default {};
</script>

<style lang="scss" scoped>
@import "../assets/stylesheets/setup";

.flex-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 2rem;
}

.gallery-container {
  margin-inline: 2rem;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0.5rem;
  max-width: 44rem;
  width: 100%;

  .gallery-image {
    border-radius: 1rem;
    height: 40vw;
    max-height: 20rem;
    transition: transform 100ms ease-in-out;

    &:hover {
      transform: scale(1.005);
    }
  }

  .rot {
    grid-column-start: 1;
    grid-column-end: 2;
    background-image: url("../assets/images/grid/rot.webp");
    // background-position: 100% 100%;
    background-size: cover;
  }
  .hochzeitsmesse {
    grid-column-start: 2;
    grid-column-end: -1;
    background-image: url("../assets/images/grid/hochzeitsmesse.webp");
    background-position: 0% 50%;
    background-size: cover;
  }
  .gruppe-grid {
    grid-column-start: 1;
    grid-column-end: 3;
    background-image: url("../assets/images/grid/gruppe-grid.webp");
    background-position: 50% 100%;
    background-size: cover;
  }
  .grün {
    grid-column-start: 1;
    grid-column-end: -1;
    background-image: url("../assets/images/grid/grün.webp");
    background-position: 0% 70%;
    background-size: cover;
  }

  .blau {
    grid-column-start: 3;
    grid-column-end: -1;
    background-image: url("../assets/images/grid/blau.webp");
    background-position: 30% 50%;
    background-size: cover;
  }
}
</style>
