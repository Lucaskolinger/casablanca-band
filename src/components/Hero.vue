<template>
  <h1 class="first-title">Hochzeit - Geburtstag - Firmenfeier</h1>
  <div class="hero-container">
    <img class="hero-img" src="../assets/images/gruppe-sw.webp" alt="" />
  </div>
</template>

<script>
import "../assets/stylesheets/global.scss";
export default {};
</script>

<style lang="scss" scoped>
@import "../assets/stylesheets/setup";

.first-title {
  color: $accent-color;
  font-weight: 600;
  width: 100%;
  text-align: center;
  height: 2rem;
  margin-top: 2rem;

  @media (min-width: $bp-sm) {
    font-size: 1.3rem;
  }
}

.hero-container {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero-img {
  width: 100%;
  max-width: 45rem;
  margin-inline: 0;
}
</style>
