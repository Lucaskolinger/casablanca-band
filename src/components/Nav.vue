<template>
  <nav class="nav">
    <img class="logo" src="logo-rot.svg" alt="casablanca" />
    <svg
      xmlns="http://www.w3.org/2000/svg"
      preserveAspectRatio="xMidYMid meet"
      viewBox="0 0 16 16"
      class="hamburger"
    >
      <path
        fill="none"
        stroke="currentColor"
        stroke-linecap="round"
        stroke-linejoin="round"
        d="M2.75 12.25h10.5m-10.5-4h10.5m-10.5-4h10.5"
      />
    </svg>
  </nav>
</template>

<script>
import "../assets/stylesheets/global.scss";
export default {};
</script>

<style lang="scss" scoped>
@import "../assets/stylesheets/setup";

.nav {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  margin-top: 2rem;
  margin-inline: 2rem;

  .logo {
    width: 5.5rem;
  }
  .hamburger {
    cursor: pointer;
    width: 2rem;
    color: $accent-color;
    stroke-width: 1px;
  }
}
</style>
