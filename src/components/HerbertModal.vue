<template>
  <div class="backdrop" @click="$emit('close-modal')">
    <div class="modal" @click.stop>
      <div class="img">
        <div class="close" @click="$emit('close-modal')">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 1024 1024"
            class="close-btn"
          >
            <path
              fill="currentColor"
              d="M512 64a448 448 0 1 1 0 896a448 448 0 0 1 0-896zm0 393.664L407.936 353.6a38.4 38.4 0 1 0-54.336 54.336L457.664 512L353.6 616.064a38.4 38.4 0 1 0 54.336 54.336L512 566.336L616.064 670.4a38.4 38.4 0 1 0 54.336-54.336L566.336 512L670.4 407.936a38.4 38.4 0 1 0-54.336-54.336L512 457.664z"
            />
          </svg>
        </div>
      </div>
      <div class="title-row">
        <h2 class="name">Herbert</h2>
        <div class="icons">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 512 512"
            class="icon tuba-icon"
          >
            <path
              fill="currentColor"
              d="M207.1 35.3c-6.5 0-12 5-12.5 11.5s4 12.3 10.4 13.4c32.2 5.3 52.9 35.2 67.7 72.9c10 25.3 17.1 54.2 22.1 83.2c24.7-5.7 47.1-5.7 64.5-4c4.9-27.6 11.8-55.1 21.4-79.2c14.8-37.7 35.5-67.6 67.7-72.9c6.4-1.1 10.9-6.9 10.4-13.4s-6-11.5-12.5-11.5H207.1zm-6 68.5c-54.3.4-109.52 32.8-109.52 99.5v159.6C91.58 443 155.2 484 219.6 484c58.3 0 116.1-34 126.3-99.7c.5-1.4.7-2.7.6-4.2v-.1c.7-5.5 1-11.2 1-17.1v-41.7c.9-17.5 2.3-37.9 4.7-59.4c-13.5-1.1-31.1-.8-50.5 4.4c2.1 20.2 3.4 39.3 4.2 55.8v40.9c0 53.1-43.5 79.1-86.3 79.1s-86.3-26-86.3-79.1V203.3c0-47.9 48.6-63.4 86.3-56.2c20.4 3.9 39.1 14.5 42.8 33.4V227c6.2-2.7 12.4-5 18.5-6.9c-2.5-13.1-5.4-26.3-8.8-39.1c-7-26.2-16-50.9-28.2-70.5c-5.3-1.8-10.8-3.2-16.5-4.3c-8.6-1.6-17.4-2.4-26.3-2.4zm-20.4 87.1c-4.5 0-8.3 3.7-8.3 8.3v4.2c0 4.6 3.8 8.4 8.3 8.4c4.6 0 8.4-3.8 8.4-8.4v-4.2c0-4.6-3.8-8.3-8.4-8.3zm25.5 0c-4.5 0-8.3 3.7-8.3 8.3v4.2c0 4.6 3.8 8.4 8.3 8.4c4.6 0 8.4-3.8 8.4-8.4v-4.2c0-4.6-3.8-8.3-8.4-8.3zm25.6 0c-4.5 0-8.3 3.7-8.3 8.3v4.2c0 4.6 3.8 8.4 8.3 8.4c4.6 0 8.4-3.8 8.4-8.4v-4.2c0-4.6-3.8-8.3-8.4-8.3zM180.7 224c-4.5 0-8.3 3.7-8.3 8.2v41.2c0 4.6 3.8 8.3 8.3 8.3c4.6 0 8.4-3.7 8.4-8.3v-41.2c0-4.5-3.8-8.2-8.4-8.2zm25.5 0c-4.5 0-8.3 3.7-8.3 8.2v41.2c0 4.6 3.8 8.3 8.3 8.3c4.6 0 8.4-3.7 8.4-8.3v-41.2c0-4.5-3.8-8.2-8.4-8.2zm25.6 0c-4.5 0-8.3 3.7-8.3 8.2v41.2c0 4.6 3.8 8.3 8.3 8.3c4.6 0 8.4-3.7 8.4-8.3v-41.2c0-4.5-3.8-8.2-8.4-8.2zm108.5 4c-23.3-.1-52.8 4.2-83.4 20v19c52-30 101.8-22 119.9-18l4.7-16c-8.5-2.2-23-4.9-41.2-5zm56.5 8l-5.2 19l20.5 9.1l8.5-24.4l-23.8-3.7zm-241 6.1c-4 8-6.4 18.8-6.4 33.9v84.1c0 40.9 34.2 62.9 69 62.9s69-22 69-62.9v-89.3c-8.2 3.2-16.6 7.2-25 12.4v76.9c0 25.6-22.4 37.6-44 37.6s-44-12-44-37.6v-62.6c-10.7-2.8-18.6-12.6-18.6-24.2v-31.2zm95.9 48.3c-.9.7-1.8 1.4-2.8 2.1c-2.3 1.8-4.9 3.1-7.6 4l-1.2.4l-.9.3v53.4c0 10.9-8.7 16.2-17.2 16.2c-11.8 0-25.3-.1-25.3-.1c5.5 8.3 15.4 12.6 25.3 12.6c14.9 0 29.7-9.7 29.7-28.7v-60.2zm-64.8 7.9v33.6c0 5.2 2.1 10.3 5.9 14.1c3.7 3.7 8.8 5.8 14.1 5.8c5.3 0 10.3-2.1 14.1-5.8c3.7-3.8 5.8-8.9 5.8-14.1v-33.6h-12.5v33.6c0 1.9-.8 3.8-2.2 5.2c-1.4 1.4-3.2 2.2-5.2 2.2s-3.9-.8-5.3-2.2c-1.4-1.4-2.2-3.3-2.2-5.2v-33.6h-12.5z"
            />
          </svg>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 512 512"
            class="icon bass-icon"
          >
            <path
              fill="currentColor"
              d="M228.2 26.89c-15.2-.25-27.7 33.46-12.3 39.8l8.9 3.61l17.8-15.5l-1.8-23.5l-8.7-3.6c-1.1-.43-2.1-.68-3.2-.78h-.7zm134.4 7.92h-2.3c-7.4.3-15.3 2.12-23.3 5.75c-21.2 9.67-43.6 32.67-59.7 75.74L174.4 394.7l-.1.2v.2c.9.5 3.6 1.9 8 4c9.8 4.8 24 15.7 26.1 38.8v.5l-1 55.6H304c-.1-17.6 1.4-34.5 8.1-51.5c11.7-29.4 39.3-54.9 97-77c0-.2 0 0 .1-.4c.3-2 .4-6 0-11c-1-10.1-4-24.9-8.6-42.2c-9.2-34.7-24.8-80.2-42.4-124.9l-2.4-6.2l5.2-4.2c36.1-28.2 51.1-56.4 53.8-79.56c2.7-23.06-6.5-41.48-21.3-52.25c-8.7-6.31-19.3-9.99-30.9-10.02zM260.5 52.44l.7 10.01l-7.6 6.6l21.7 8.93c1.2-2.17 2.5-4.28 3.8-6.33l4-9.89zm69 18.56c8.8 0 16 7.16 16 16s-7.2 16-16 16s-16-7.16-16-16s7.2-16 16-16zm-136.7 49.7c-15.2-.3-27.9 33.4-12.3 39.8l8.8 3.6l17.8-15.5l-1.7-23.6l-8.8-3.6c-1.1-.4-2.1-.6-3.1-.7zm32.2 25.5l.7 10l-7.6 6.6l19.9 8.1l6.2-16.8zm71.6 19.8c8.8 0 16 7.2 16 16s-7.2 16-16 16s-16-7.2-16-16s7.2-16 16-16zm-139.8 50.6c-15.3-.3-27.8 33.4-12.4 39.8l8.9 3.6l17.8-15.5l-1.8-23.6l-8.7-3.6c-1.1-.4-2.1-.6-3.1-.7zm32.2 25.5l.7 10l-7.6 6.6l20.4 8.3l6.2-16.8zm67.2 19.3c8.8 0 16 7.2 16 16s-7.2 16-16 16s-16-7.2-16-16s7.2-16 16-16zm-140.1 54.4c-15.2-.3-27.78 33.4-12.3 39.8l8.8 3.6l17.8-15.5l-1.8-23.6l-8.7-3.6c-1.1-.4-2.1-.6-3.1-.7zm32.2 25.5l.7 10l-7.6 6.6l22.8 9.3l6.8-16.6zm69.3 18.5c8.8 0 16 7.2 16 16s-7.2 16-16 16s-16-7.2-16-16s7.2-16 16-16z"
            />
          </svg>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 32 32"
            class="icon mikro-icon"
          >
            <path
              fill="currentColor"
              d="M23 14v3a7 7 0 0 1-14 0v-3H7v3a9 9 0 0 0 8 8.94V28h-4v2h10v-2h-4v-2.06A9 9 0 0 0 25 17v-3Z"
            />
            <path
              fill="currentColor"
              d="M16 22a5 5 0 0 0 5-5V7a5 5 0 0 0-10 0v10a5 5 0 0 0 5 5Z"
            />
          </svg>
        </div>
      </div>
      <p class="text">
        Unser Herbert beherrscht nicht nur den richtigen Groove auf seinen
        Bass-Saiten, sondern sorgt auch mit seiner Tuba beim Brautverziehen für
        die richtige Bierzelt- Stimmung. Wenn er dann noch sein "Bobfahrerlied"
        oder "Sonne in der Nacht" zum Besten gibt, bleibt keiner mehr auf den
        Stühlen sitzen.
      </p>
    </div>
  </div>
</template>

<script>
import "../assets/stylesheets/global.scss";
export default {};
</script>

<style lang="scss" scoped>
@import "../assets/stylesheets/setup";

.backdrop {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #000000da;
  z-index: 1;

  .modal {
    background-color: rgb(220, 220, 220);
    border-radius: 2.2rem;
    width: 80vw;
    max-width: 30rem;
    z-index: 2;
    filter: drop-shadow(0px 0px 90px rgba(213, 27, 76, 0.5));

    .img {
      aspect-ratio: 16/14;
      background-image: url("../assets/images/portraits/herbert-2.webp");
      background-position: 0% 25%;
      background-size: cover;
      position: relative;
      border-top-right-radius: 2rem;
      border-top-left-radius: 2rem;

      .close {
        cursor: pointer;
        position: absolute;
        right: 0;
        color: gray;
        margin-right: 1rem;
        margin-top: 1rem;
        transition: color 150ms ease-in-out;

        &:hover {
          color: $accent-color;
        }

        .close-btn {
          width: 2rem;
        }
      }
    }

    .title-row {
      display: flex;
      margin-bottom: 1rem;
      margin-top: 1rem;
      margin-left: 1.5rem;
      margin-right: 2rem;
      align-items: center;
      justify-content: space-between;

      .name {
        font-size: 2rem;
        font-weight: 700;
      }

      .icons {
        display: flex;
        align-items: center;
        gap: 0.5rem;

        .icon {
          width: 2rem;
          color: $accent-color;
          transition: transform 200ms ease-in-out;

          &:hover {
            transform: translateY(-0.25rem);
          }
        }
      }
    }

    .text {
      padding: 0 1.5rem 2rem 1.5rem;
      font-size: 1rem;
      line-height: 1.3;
    }
  }
}
</style>
