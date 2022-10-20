<template>
  <div class="grid-flex-wrapper">
    <div class="repertoire-container">
      <div class="rubrik kuscheln">
        <h2 class="rubrik-title">Zum Kuscheln</h2>
        <div class="hp-container">
          <Hörprobe
            :playbutton="false"
            title="Zam oid wearn"
            musician="Edmund"
          />
          <Hörprobe
            :playbutton="false"
            title="Shallow"
            musician="Br Cooper & Lady Gaga"
          />
          <Hörprobe
            :playbutton="false"
            title="So liab hob i di"
            musician="Andreas Gabalier"
          />
        </div>
      </div>
      <div class="rubrik party">
        <h2 class="rubrik-title">Zum Party Machen</h2>
        <div class="hp-container">
          <Hörprobe
            :playbutton="false"
            title="A night like this"
            musician="Caro Emerald"
          />
          <Hörprobe
            :playbutton="false"
            title="Stumblin' in"
            musician="Suzy Quatro & Chris Norman"
          />
          <Hörprobe
            :playbutton="false"
            title="It's so easy"
            musician="Linda Ronstadt"
          />
        </div>
      </div>
      <div class="rubrik tanzen">
        <h2 class="rubrik-title">Zum Tanzen und Lustig-Sein</h2>
        <div class="hp-container">
          <Hörprobe
            :playbutton="false"
            title="Westerland"
            musician="Die Ärzte"
          />
          <Hörprobe
            :playbutton="false"
            title="Atemlos"
            musician="Helene Fischer"
          />
          <Hörprobe
            :playbutton="false"
            title="Simply the best"
            musician="Tina Turner"
          />
        </div>
      </div>
      <div class="rubrik haut">
        <h2 class="rubrik-title">Zum "Aus-Der-Haut-Fahren"</h2>
        <div class="hp-container">
          <Hörprobe
            :playbutton="false"
            title="Highway to hell"
            musician="ACDC"
          />
          <Hörprobe
            :playbutton="false"
            title="Final Countdown"
            musician="Europe"
          />
          <Hörprobe
            :playbutton="false"
            title="We will rock you"
            musician="Queen"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "../assets/stylesheets/global.scss";
import Hörprobe from "../components/Hörprobe.vue";
export default {
  components: {
    Hörprobe,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/stylesheets/setup";

.grid-flex-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-block: 2rem;
}

.repertoire-container {
  color: $accent-color;
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
  width: 100%;
  max-width: 44rem;
  margin-inline: 2rem;

  @media (min-width: $bp-sm) {
    grid-template-columns: 1fr 1fr;
  }

  .rubrik-title {
    margin-bottom: 1rem;
    font-weight: 700;
    font-size: 1rem;
  }

  .hp-container {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }
}
</style>
