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
        <h2 class="name">Markus</h2>
        <div class="icons">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="icon"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 512 512"
          >
            <path
              fill="currentColor"
              d="m376.3 30.6l-63.3 3L61.43 230.9l261.47-51.5c5.8-4.6 10.9-9 15.4-13.1L302 75.6l15.5-6.2l33.7 84.2c55.1-60.2-20.4-71.1 25.1-123zM357 168l-13.2 11.9l9.6 24.1c-9.1-.4-19.2-.6-30.5-.7L61.43 254.9s.34 2.2.84 5.5c2.36 15.5-7.73 30.2-23.07 33.6c-8.93 2-16.61 3.7-16.61 3.7l3.95 21.2l334.16 30.5l126-53.9l-.9-43.4c-81.1-8.7-11.4-39.4-114-47L357 168zM83.78 284.8L358.4 307l-18.1 16.1l-280.68-25.9l24.16-12.4zm-1.35 53.6l13.65 97.1l-3.47 6.2l.36 15.8l17.13 1.6l17.1-6.2v-13.2l-4.8-3.9l9.1-93l-49.07-4.4zM184 350.5V426l105.2 9v-75.2l-16.7-1.5V417l-71.8-6v-59l-16.7-1.5zm209.8 2.7l-29.4 10.9l-24.8-2l15.6 99.4l-3.9 5.1l.8 18l17.1 1.7l15.9-7.4l.3-13.2l-3.9-3.9l12.3-108.6zm-208.7 89.6l-28.4 9.5l3.1 14.4l102.3 10.1l21-7.4l1.1-18.3l-99.1-8.3z"
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
        </div>
      </div>
      <p class="text">
        Nachdem der klassische Geigenunterricht doch nicht das Richtige für ihn
        war, hat er schnell herausgefunden, dass er ebenso wie Elton John oder
        Jerry Lee Lewis das Piano bearbeiten will. Und das macht er jetzt auch
        genauso perfekt wie seine großen Vorbilder.
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
      background-image: url("../assets/images/portraits/markus-2.webp");
      background-position: 0% 0%;
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
