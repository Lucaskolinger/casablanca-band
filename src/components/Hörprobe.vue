<template>
  <article class="hörproben-container">
    <svg
      v-if="playbutton"
      xmlns="http://www.w3.org/2000/svg"
      preserveAspectRatio="xMidYMid meet"
      viewBox="0 0 1024 1024"
      class="play-btn"
    >
      <path
        fill="currentColor"
        d="M512 64C264.6 64 64 264.6 64 512s200.6 448 448 448s448-200.6 448-448S759.4 64 512 64zm144.1 454.9L437.7 677.8a8.02 8.02 0 0 1-12.7-6.5V353.7a8 8 0 0 1 12.7-6.5L656.1 506a7.9 7.9 0 0 1 0 12.9z"
      />
    </svg>

    <div v-else class="playbutton-placeholder"></div>
    <h2 class="title">{{ title }}</h2>
    <p class="musician">{{ musician }}</p>
  </article>

  <!-- <iframe
    width="0"
    class="yt-iframe"
    height="0"
    src="https://www.youtube.com/embed/ycTImOGZ4rY"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe> -->
</template>

<script>
import "../assets/stylesheets/global.scss";
export default {
  props: {
    playbutton: Boolean,
    title: String,
    musician: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/stylesheets/setup";

.hörproben-container {
  display: flex;
  background-color: $accent-color;
  align-items: center;
  padding: 1rem;
  color: white;
  border-radius: 1rem;

  .play-btn {
    width: 2rem;
    cursor: pointer;
    margin-right: 0.5rem;
    flex: none;
  }
  .playbutton-placeholder {
    width: 2rem;
    height: 2rem;
  }
  .title {
    font-size: 1rem;
    line-height: 1.4;
  }
  .musician {
    opacity: 0.8;
    font-size: 0.75rem;
    font-weight: 500;
    line-height: 1.4;
    margin-left: auto;
    text-align: right;
  }
}
</style>
