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
        <h2 class="name">Julia</h2>
        <div class="icons">
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
            viewBox="0 0 32 32"
            class="icon"
          >
            <g fill="currentColor">
              <path
                d="M19.813 11.203a1.29 1.29 0 0 0-1.184.346l-1.07 1.07c-.5.5-.5 1.32 0 1.82s1.32.5 1.82 0l1.07-1.07c.32-.32.435-.77.346-1.184l8.874-8.376c.43-.4.44-1.08.02-1.5c-.42-.42-1.1-.41-1.5.02l-8.376 8.874Zm-7.628 0a1.29 1.29 0 0 1 1.184.346l1.07 1.07c.5.5.5 1.32 0 1.82s-1.32.5-1.82 0l-1.07-1.07a1.29 1.29 0 0 1-.346-1.184L2.329 3.809c-.43-.4-.44-1.08-.02-1.5c.42-.42 1.1-.41 1.5.02l8.376 8.874ZM10.187 7.63a7.928 7.928 0 0 1 5.752-2.471a7.92 7.92 0 0 1 5.812 2.534l1.206-1.278a9.675 9.675 0 0 0-7.018-3.006a9.671 9.671 0 0 0-6.96 2.94l1.208 1.28Z"
              />
              <path
                d="m6.923 9.52l1.4 1.322a7.864 7.864 0 0 0-.324 2.257c0 4.38 3.56 7.94 7.94 7.94c4.38 0 7.94-3.56 7.94-7.94c0-.75-.105-1.478-.3-2.167l1.407-1.328a9.67 9.67 0 0 1 .653 3.505h.02v4.639c.007.173.01.345.01.518c0 6.488-4.36 11.734-9.73 11.734c-5.156 0-9.366-4.829-9.708-10.931a9.865 9.865 0 0 1-.022-1.245V13.11h.03a9.69 9.69 0 0 1 .684-3.588Zm14.85 11.341v5.048c0 .045.003.09.01.134a9.78 9.78 0 0 0 1.742-1.693v-5.194a9.75 9.75 0 0 1-1.752 1.705Zm-5.834 1.948c-.296 0-.588-.013-.877-.04v5.192a9.85 9.85 0 0 0 1.753-.002v-5.19a9.806 9.806 0 0 1-.876.04Zm-7.586-3.653v5.22a9.784 9.784 0 0 0 1.74 1.68a.88.88 0 0 0 .012-.147V20.86a9.748 9.748 0 0 1-1.752-1.705Z"
              />
            </g>
          </svg>
        </div>
      </div>
      <p class="text">
        Oldies? Klassiker? Schlager? Hits von heute? Dank ihrer vielseitigen
        Fähigkeiten für unsere Julia alles kein Problem. Von "Atemlos" (Helene
        Fischer), über "Simply the Best" (Tina Turner) bis hin zu "Shallow"
        (Lady Gaga & Bradley Cooper) verleiht Julia mit ihrer Top-Stimme jedem
        Song den perfekten Live- Sound, bei dem keiner ruhig auf seinem Stuhl
        sitzenbleiben kann.
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
      background-image: url("../assets/images/portraits/julia-2.webp");
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
