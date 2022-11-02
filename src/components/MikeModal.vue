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
        <h2 class="name">Mike</h2>
        <div class="icons">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 32 32"
            class="icon"
          >
            <path
              fill="currentColor"
              d="M23.017 5.719a1 1 0 0 1 1.103-.886l4.97.545a1 1 0 0 1 .885 1.103L27.69 27.356a1 1 0 0 1-1.103.885l-4.97-.544A1 1 0 0 1 20.77 27h-.053l.382-20.999a3.98 3.98 0 0 1 1.833.496l.085-.778Zm4.147 3.472a.5.5 0 1 0 .108-.995a.5.5 0 0 0-.108.995Zm-2.097.776a.5.5 0 1 0 .108-.994a.5.5 0 0 0-.108.994Zm-.327 2.982a.5.5 0 1 0 .109-.994a.5.5 0 0 0-.109.994Zm-.102 5.522a.5.5 0 1 0-.994-.109a.5.5 0 0 0 .994.109Zm-.878 3.425a.5.5 0 1 0 .11-.994a.5.5 0 0 0-.11.994Zm-.326 2.982a.5.5 0 1 0 .108-.994a.5.5 0 0 0-.108.994Zm1.53-9.39a.5.5 0 1 0-.993-.108a.5.5 0 0 0 .994.109Zm1.118 8.17a.5.5 0 1 0-.994-.108a.5.5 0 0 0 .994.109Zm-.225-2.539a.5.5 0 1 0 .11-.994a.5.5 0 0 0-.11.994Zm.878-3.424a.5.5 0 1 0-.994-.11a.5.5 0 0 0 .994.11Zm-.225-2.54a.5.5 0 1 0 .11-.994a.5.5 0 0 0-.11.994Zm.878-3.425a.5.5 0 1 0-.994-.109a.5.5 0 0 0 .994.11ZM18.379 6h1.72l-.382 20.953v-.003L18.38 6Zm-2.96 0h1.958l1.341 21h-.03a.492.492 0 0 0-.006-.096L15.418 6Zm-1.005.043l3.227 20.67l.05.202a1 1 0 0 1-.729 1.212L8.23 30.305a1 1 0 0 1-1.212-.729L1.938 9.2a1 1 0 0 1 .728-1.212l8.732-2.177a1 1 0 0 1 1.213.728l.053.214a3.979 3.979 0 0 1 1.75-.71Zm-11.386 3.4l.242.97a.5.5 0 0 0 .606.365l2.437-.608a.5.5 0 0 1 .379-.502l2.425-.605l.096.384l-.484-1.94l-5.336 1.33a.5.5 0 0 0-.365.606Zm3.298.827l-2.425.605a.5.5 0 0 0-.364.606l.241.97a.5.5 0 0 0 .607.364l2.425-.604a.5.5 0 0 1 .366-.602l2.425-.605l.12.48l-.484-1.94l.122.49l-2.425.605a.5.5 0 0 1-.607-.365v-.004Zm.517 2.035l-2.434.607a.5.5 0 0 0-.364.606l.241.97a.5.5 0 0 0 .607.365l5.336-1.33l-.484-1.941l.098.392l-2.426.605a.5.5 0 0 1-.574-.274Zm-2.29 3.251l.241.97a.5.5 0 0 0 .607.365l2.444-.61a.5.5 0 0 1 .378-.524l2.413-.602l-.383-1.536l-5.336 1.331a.5.5 0 0 0-.364.606Zm6.325.57l-2.413.601a.5.5 0 0 1-.602-.347l-2.438.608a.5.5 0 0 0-.364.606l.241.97a.5.5 0 0 0 .607.364l2.454-.612a.5.5 0 0 1 .36-.624l2.397-.597l-.242-.97ZM8.401 18.41l-2.468.615a.5.5 0 0 0-.364.606l.242.97a.5.5 0 0 0 .606.365l2.425-.605a.5.5 0 0 1 .365-.606l2.425-.605l.121.485l-.391-1.57l-2.397.597a.5.5 0 0 1-.564-.252Zm.475 2.046l-2.435.607a.5.5 0 0 0-.364.606l.242.97a.5.5 0 0 0 .606.364l5.336-1.33l-.484-1.94l.097.388l-2.426.604a.5.5 0 0 1-.572-.27Zm-2.291 3.25l.242.97a.5.5 0 0 0 .606.365l2.503-.624v-.003a.5.5 0 0 1 .363-.606l2.349-.585l-.363-1.453L6.95 23.1a.5.5 0 0 0-.364.606Zm3.385.805l-2.513.627a.5.5 0 0 0-.364.606l.242.97a.5.5 0 0 0 .606.365l2.45-.611a.5.5 0 0 1 .373-.56l2.404-.599l-.278-1.116l-2.349.586a.5.5 0 0 1-.571-.268Zm.445 2.054l-2.45.61a.5.5 0 0 0-.364.607l.242.97a.5.5 0 0 0 .606.364l5.336-1.33l-.375-1.506l-2.404.599a.5.5 0 0 1-.59-.314Z"
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
            class="icon"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 24 24"
          >
            <path
              fill="currentColor"
              fill-rule="evenodd"
              d="M22 21a2 2 0 0 0 2-2V5a2 2 0 0 0-2-2H3a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h19ZM11 5H8.985v8h-1v6H12v-6h-1V5Zm7.015 14H22V5h-2.985v8h-1v6Zm-1-6h-1V5H14v8h-1v6h4.015v-6Zm-10.03 6v-6h-1V5H3v14h3.985Z"
              clip-rule="evenodd"
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
        Er kümmert sich mit viel Hingabe und Liebe zum Detail um die echten
        Keyboardsounds. Nebenbei sorgt er unter anderem bei Brautentführungen
        für die richtige "Wein-Stimmung". Unzählige Geschichten und Witze hat
        Mike jederzeit spontan auf Lager.
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
  z-index: 2;

  .modal {
    background-color: rgb(220, 220, 220);
    border-radius: 2.2rem;
    width: 80vw;
    max-width: 30rem;
    z-index: 3;
    filter: drop-shadow(0px 0px 90px rgba(213, 27, 76, 0.5));

    .img {
      aspect-ratio: 16/14;
      background-image: url("../assets/images/portraits/mike-1.webp");
      background-position: 0% 10%;
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
