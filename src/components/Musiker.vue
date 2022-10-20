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
      <img
        class="portrait"
        @click="showHerbertModal = true"
        src="../assets/images/portraits/herbert-1.webp"
        alt=""
      />
      <img
        class="portrait"
        @click="showMarkusModal = true"
        src="../assets/images/portraits/markus-1.webp"
        alt=""
      />
      <img
        class="portrait"
        @click="showChrisModal = true"
        src="../assets/images/portraits/chris-1.webp"
        alt=""
      />
      <img
        class="portrait"
        @click="showMartinModal = true"
        src="../assets/images/portraits/martin-1.webp"
        alt=""
      />
      <img
        class="portrait"
        @click="showMikeModal = true"
        src="../assets/images/portraits/mike-1.webp"
        alt=""
      />
      <img
        class="portrait"
        @click="showJuliaModal = true"
        src="../assets/images/portraits/julia-1.webp"
        alt=""
      />
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
  .portrait {
    cursor: pointer;
    width: 100%;
    border-radius: 2rem;
    transition: transform 100ms ease-in-out;
    filter: drop-shadow(0px 0px 20px #000);

    &:hover {
      transform: translate(0rem, -0.5rem);
    }
  }
}
</style>
