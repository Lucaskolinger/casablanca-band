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
        <h2 class="name">Martin</h2>
        <div class="icons">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 512 512"
            class="icon"
          >
            <path
              fill="currentColor"
              d="M502.63 39L473 9.37a32 32 0 0 0-45.26 0L381.46 55.7a35.14 35.14 0 0 0-8.53 13.79L360.77 106l-76.26 76.26c-12.16-8.76-25.5-15.74-40.1-19.14c-33.45-7.78-67-.88-89.88 22a82.45 82.45 0 0 0-20.24 33.47c-6 18.56-23.21 32.69-42.15 34.46c-23.7 2.27-45.73 11.45-62.61 28.44C-16.11 327-7.9 409 47.58 464.45S185 528 230.56 482.52c17-16.88 26.16-38.9 28.45-62.71c1.76-18.85 15.89-36.13 34.43-42.14a82.6 82.6 0 0 0 33.48-20.25c22.87-22.88 29.74-56.36 22-89.75c-3.39-14.64-10.37-28-19.16-40.2L406 151.23l36.48-12.16a35.14 35.14 0 0 0 13.79-8.53l46.33-46.32a32 32 0 0 0 .03-45.22zM208 352a48 48 0 1 1 48-48a48 48 0 0 1-48 48z"
            />
          </svg>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 24 24"
            class="icon"
          >
            <path
              fill="currentColor"
              d="M4 2a1 1 0 0 0-1 1a1 1 0 0 0 1 1a3 3 0 0 1 3 3v8.5c0 3.6 2.9 6.5 6.5 6.5s6.5-2.9 6.5-6.5V13a1 1 0 0 0 1-1a1 1 0 0 0-1-1h-6a1 1 0 0 0-1 1a1 1 0 0 0 1 1v2a1 1 0 0 1-1 1a1 1 0 0 1-1-1v-4a1 1 0 0 0 1-1a1 1 0 0 0-1-1V8a1 1 0 0 0 1-1a1 1 0 0 0-1-1v-.5A3.5 3.5 0 0 0 8.5 2H4Z"
            />
          </svg>
        </div>
      </div>
      <p class="text">
        Martin ist unser musikalisches Genie. Alle Instrumente spielt er absolut
        perfekt. Er ist das musikalische Herz der Band, schreibt alle Chöre und
        hört jeden falschen Ton.
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
      background-image: url("../assets/images/portraits/martin-2.webp");
      background-position: 0% 20%;
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
