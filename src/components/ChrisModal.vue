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
        <h2 class="name">Chris</h2>
        <div class="icons">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 512 512"
            class="icon"
          >
            <path
              fill="currentColor"
              d="m111 58.3l-87.37.4l-.61 8.3L192.4 92.6l1.8-8.1zm310.8 18.8l-.3 29.7l5-.8l4.9.8l-.3-29.7zM96.33 92.8l-1.81 13l-33.17 26.4l1.84 115.6l6.16-40.4l9.55-2.3h.28l-1.03-65l31.95-25.4l2.7-19.4zm330.17 25.9l-66.6 10.4l.6 8.3h132l.6-8.3zm-66 33.3l-.6 8.3l66.6 10.4l66.6-10.4l-.6-8.3zm60.3 30.5l-.2 20.8c2.8.5 5.6 1.2 8.5 1.8l3.3.8l-.2-23.4l-5.7.9zm-287.4 30.7c-16.5-.2-33.5 1.9-51.1 6.1l-2.86 18.8c23.26-3.3 75.96-6.9 127.56 14.6c4-1.6 8.2-3.1 12.4-4.3l1.2-8c-26.6-18.2-55.8-26.8-87.2-27.2zm241.2 0c-31.4.4-60.6 9-87.2 27.2l1.2 8c4.2 1.2 8.4 2.7 12.4 4.3c51.6-21.5 104.3-17.9 127.6-14.6l-2.9-18.8c-17.6-4.2-34.6-6.3-51.1-6.1zm-258.1 39c-17.91 0-32.1 1.8-39.69 3.1l-7.05 46.3l72.94 11.1c10.1-20.3 25.5-37.5 44.5-49.6c-25.4-8.5-50.4-10.9-70.7-10.9zm275 0c-20.3 0-45.3 2.4-70.7 10.9c19 12.1 34.4 29.3 44.5 49.6l72.9-11.1l-7-46.3c-7.6-1.3-21.8-3.1-39.7-3.1zm-137.5 10c-49.9 0-90.4 40.5-90.4 90.4c0 49.9 40.5 90.4 90.4 90.4c49.9 0 90.4-40.5 90.4-90.4c0-49.9-40.5-90.4-90.4-90.4zM64.27 315.5l1.36 85.5l-46.73 87h18.94l33.24-62l15.19 62h17.23l-21.19-86l-1.33-84zM433.6 317l-14.2 2.2l-.8 74.1l-24.2 55.7l7.4 25l24.7-57l30.9 71h18.2l-41.2-94.7zm-279.7 11.6c-4.7 12.1-7.2 25.2-7.2 38.9C146.7 427 194.8 475 254 475c59.2 0 107.3-48 107.3-107.5c0-13.7-2.5-26.8-7.2-38.9c1.8 7.7 2.8 15.8 2.8 24C356.9 409 310.8 456 254 456c-56.8 0-102.9-47-102.9-103.4c0-8.2 1-16.3 2.8-24zm-18 77.4l-20.2 82h25.7l11.8-48c-7.4-11-13.3-22-17.3-34zm236.2 0c-4 12-9.9 23-17.3 34l11.8 48h25.7z"
            />
          </svg>
        </div>
      </div>
      <p class="text">
        Unser Taktgeber ist mit 32 der Jüngste im Bunde. Er senkt nicht nur den
        Altersdurchschnitt, sondern sorgt mit seinen Drums für den richtigen
        Drive. Vom klassischen Walzer über Rock'n Roll und Rock Medley bis hin
        zu romantischen Balladen hat er immer die passenden Beats und Effekte
        parat.
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
      background-image: url("../assets/images/portraits/chris-2.webp");
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
