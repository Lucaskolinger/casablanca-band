<template>
  <div class="flex-wrapper">
    <section class="gallery-container">
      <div class="gallery-image gruppe-geigenkasten"></div>
      <div class="gallery-image chris-stehend"></div>
      <div class="gallery-image gruppe-geiger"></div>
      <div class="gallery-image chris-trommel"></div>
      <div class="gallery-image gruppe-socken"></div>
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
  .gruppe-geiger {
    grid-column-start: 1;
    grid-column-end: -1;
    background-image: url("../assets/images/grid/gruppe-geiger.webp");
    background-position: 0% 50%;
    background-size: cover;
  }
  .gruppe-geigenkasten {
    grid-column-start: 1;
    grid-column-end: 2;
    background-image: url("../assets/images/grid/chris-trommel.webp");
    // background-position: 100% 100%;
    background-size: cover;
  }
  .gruppe-socken {
    grid-column-start: 3;
    grid-column-end: -1;
    background-image: url("../assets/images/grid/gruppe-socken.webp");
    background-position: 0% 50%;
    background-size: cover;
  }
  .chris-stehend {
    grid-column-start: 2;
    grid-column-end: -1;
    background-image: url("../assets/images/grid/hochzeitsmesse.webp");
    background-position: 0% 50%;
    background-size: cover;
  }
  .chris-trommel {
    grid-column-start: 1;
    grid-column-end: 3;
    background-image: url("../assets/images/grid/gruppe-geigenkasten.webp");
    background-position: 50% 100%;
    background-size: cover;
  }
}
</style>
