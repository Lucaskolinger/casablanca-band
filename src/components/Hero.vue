<template>
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
