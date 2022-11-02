<template>
  <article class="hörproben-container">
    <div class="play-btn" v-if="playbutton">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        preserveAspectRatio="xMidYMid meet"
        viewBox="0 0 1024 1024"
        v-if="isPlaying === true"
        @click="handleClickOnPlay"
      >
        <path
          fill="currentColor"
          d="M512 64C264.6 64 64 264.6 64 512s200.6 448 448 448s448-200.6 448-448S759.4 64 512 64zm144.1 454.9L437.7 677.8a8.02 8.02 0 0 1-12.7-6.5V353.7a8 8 0 0 1 12.7-6.5L656.1 506a7.9 7.9 0 0 1 0 12.9z"
        />
      </svg>

      <svg
        xmlns="http://www.w3.org/2000/svg"
        v-else
        @click="handleClickOnPause"
        preserveAspectRatio="xMidYMid meet"
        viewBox="0 0 1024 1024"
      >
        <path
          fill="currentColor"
          d="M512 64C264.6 64 64 264.6 64 512s200.6 448 448 448s448-200.6 448-448S759.4 64 512 64zm-80 600c0 4.4-3.6 8-8 8h-48c-4.4 0-8-3.6-8-8V360c0-4.4 3.6-8 8-8h48c4.4 0 8 3.6 8 8v304zm224 0c0 4.4-3.6 8-8 8h-48c-4.4 0-8-3.6-8-8V360c0-4.4 3.6-8 8-8h48c4.4 0 8 3.6 8 8v304z"
        ></path>
      </svg>
    </div>

    <div v-else class="playbutton-placeholder"></div>
    <h2 class="title">{{ title }}</h2>
    <p class="musician">{{ musician }}</p>
    <iframe
      v-if="insertPlayer"
      width="0"
      height="0"
      :src="ytLink"
      title="YouTube video player"
      frameborder="0"
      allow="autoplay"
    >
    </iframe>
  </article>
</template>

<script>
import "../assets/stylesheets/global.scss";
export default {
  props: {
    playbutton: Boolean,
    title: String,
    musician: String,
    ytLink: String,
    timeout: String,
  },
  data() {
    return {
      isPlaying: true,
      insertPlayer: false,
      // title: this.$props.title,
    };
  },
  methods: {
    handleClickOnPlay() {
      this.insertPlayer = true;
      this.isPlaying = false;
      this.$emit("clickedOnPlay", this.title);
      setTimeout(() => {
        this.insertPlayer = false;
        this.isPlaying = true;
      }, parseInt(this.timeout));
    },
    handleClickOnPause() {
      this.insertPlayer = false;
      this.isPlaying = true;
    },
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
    margin-right: 0.5rem;
    flex: none;
    cursor: pointer;

    svg {
      width: 100%;
    }
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
    max-width: 6rem;
  }
}
</style>
