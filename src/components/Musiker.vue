<template>
  <Transition>
    <HerbertModal
      v-show="showHerbertModal"
      @close-modal="showHerbertModal = false"
    />
  </Transition>

  <Transition>
    <MarkusModal
      v-show="showMarkusModal"
      @close-modal="showMarkusModal = false"
    />
  </Transition>

  <Transition>
    <ChrisModal v-show="showChrisModal" @close-modal="showChrisModal = false" />
  </Transition>

  <Transition>
    <MartinModal
      v-show="showMartinModal"
      @close-modal="showMartinModal = false"
    />
  </Transition>

  <Transition>
    <MikeModal v-show="showMikeModal" @close-modal="showMikeModal = false" />
  </Transition>

  <Transition>
    <JuliaModal v-show="showJuliaModal" @close-modal="showJuliaModal = false" />
  </Transition>

  <div class="background"></div>

  <div class="grid-flex-wrapper">
    <section class="musiker-grid">
      <div class="portrait-wrapper">
        <span @click="showHerbertModal = true">+</span>
        <img
          class="portrait"
          @click="showHerbertModal = true"
          src="../assets/images/portraits/herbert-2.webp"
          alt=""
        />
      </div>
      <div class="portrait-wrapper">
        <span @click="showMarkusModal = true">+</span>
        <img
          class="portrait"
          @click="showMarkusModal = true"
          src="../assets/images/portraits/markus-1.webp"
          alt=""
        />
      </div>
      <div class="portrait-wrapper">
        <span @click="showChrisModal = true">+</span>
        <img
          class="portrait"
          @click="showChrisModal = true"
          src="../assets/images/portraits/chris-1.webp"
          alt=""
        />
      </div>
      <div class="portrait-wrapper">
        <span @click="showMartinModal = true">+</span>
        <img
          class="portrait"
          @click="showMartinModal = true"
          src="../assets/images/portraits/martin-1.webp"
          alt=""
        />
      </div>
      <div class="portrait-wrapper">
        <span @click="showMikeModal = true">+</span>
        <img
          class="portrait"
          @click="showMikeModal = true"
          src="../assets/images/portraits/mike-1.webp"
          alt=""
        />
      </div>
      <div class="portrait-wrapper">
        <span @click="showJuliaModal = true">+</span>
        <img
          class="portrait"
          @click="showJuliaModal = true"
          src="../assets/images/portraits/julia-2.webp"
          alt=""
        />
      </div>
    </section>
  </div>
</template>

<script>
import "../assets/stylesheets/global.scss";
import HerbertModal from "./HerbertModal.vue";
import MarkusModal from "./MarkusModal.vue";
import ChrisModal from "./ChrisModal.vue";
import MartinModal from "./MartinModal.vue";
import MikeModal from "./MikeModal.vue";
import JuliaModal from "./JuliaModal.vue";

export default {
  components: {
    HerbertModal,
    MarkusModal,
    ChrisModal,
    MartinModal,
    MikeModal,
    JuliaModal,
  },
  data() {
    return {
      showHerbertModal: false,
      showMarkusModal: false,
      showChrisModal: false,
      showMartinModal: false,
      showMikeModal: false,
      showJuliaModal: false,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/stylesheets/setup";

.v-enter-active,
.v-leave-active {
  transition: opacity 0.3s ease-in-out;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

.background {
  width: 100vw;
  height: 60rem;
  background: linear-gradient($accent-color, white);
  position: absolute;
  z-index: -1;
  border-bottom-left-radius: 2rem;
  border-bottom-right-radius: 2rem;
}

.grid-flex-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
}

.musiker-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.5rem;
  margin-inline: 2rem;
  max-width: 44rem;

  @media (min-width: $bp-sm) {
    grid-template-columns: 1fr 1fr 1fr;
  }

  .portrait-wrapper {
    position: relative;
    transition: all 100ms ease-in-out;

    // &:hover {
    //   -webkit-transform: scale(1.05);
    // }

    span {
      position: absolute;
      top: 1rem;
      right: 1rem;
      z-index: 1;
      color: black;
      background-color: rgb(231, 228, 228);
      opacity: 0.8;
      height: 2rem;
      width: 2rem;
      text-align: center;
      border-radius: 100%;
      font-size: 2rem;
      cursor: pointer;
      transition: all 200ms ease-in-out;

      &:hover {
        transform: scale(1.1);
        background-color: $accent-color;
      }
    }
  }

  .portrait {
    width: 100%;
    border-radius: 2rem;
    filter: drop-shadow(0px 0px 20px #000);
  }
}
</style>
