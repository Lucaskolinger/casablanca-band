<template>
  <div class="grid-flex-wrapper">
    <div class="repertoire-container">
      <div class="rubrik kuscheln">
        <h2 class="rubrik-title">Zum Kuscheln</h2>
        <div class="hörproben-column">
          <Hörprobe
            :playbutton="false"
            title="Zam oid wearn"
            musician="Edmund"
          />
          <Hörprobe
            :playbutton="true"
            title="Shallow"
            ytLink="https://www.youtube.com/embed/OdWTuQgtfvU?autoplay=1&showinfo=0&controls=0&mute=0"
            musician="Br Cooper & Lady Gaga"
            timeout="140000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
          />
          <Hörprobe
            :playbutton="false"
            title="So liab hob i di"
            musician="Andreas Gabalier"
          />
          <Hörprobe
            :playbutton="true"
            title="Just give me a reason"
            musician="Pink feat. Nate Ruess"
            ytLink="https://www.youtube.com/embed/NP0V5fG9WJc?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="140000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
          />
          <Hörprobe
            :playbutton="true"
            title="Love on the brain"
            musician="Rihanna"
            ytLink="https://www.youtube.com/embed/ViJAg6-PFKI?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="95000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
          />
          <Hörprobe
            :playbutton="true"
            title="You are the sunshine of my life"
            musician="Stevie Wonder"
            ytLink="https://www.youtube.com/embed/u9jn0OvFtdA?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="170000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
          />
          <Hörprobe
            :playbutton="true"
            title="Ohne Dich"
            musician="Münchner Freiheit"
            ytLink="https://www.youtube.com/embed/hMTpc_BqcN8?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="80000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
          />
        </div>
      </div>
      <div class="rubrik party">
        <h2 class="rubrik-title">Zum Party Machen</h2>
        <div class="hörproben-column">
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
          <Hörprobe
            :playbutton="false"
            title="Expresso & Tschianti"
            musician="Josh"
          />
          <Hörprobe
            :playbutton="true"
            title="Long Train Running"
            musician="Doobie Brothers"
            ytLink="https://www.youtube.com/embed/9xKdcBdn5hQ?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="110000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
          />
          <Hörprobe
            :playbutton="true"
            title="Mit 66 Jahren"
            musician="Udo Jürgens"
            ytLink="https://www.youtube.com/embed/PVHqyxd6jxU?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="80000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
          />
          <Hörprobe
            :playbutton="true"
            title="Fuck you"
            musician="Cee Lo Green"
            ytLink="https://www.youtube.com/embed/iZVFxlPk6aY?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="60000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
          />
          <Hörprobe
            :playbutton="true"
            title="Ein Kompliment"
            musician="Sportfreunde Stiller"
            ytLink="https://www.youtube.com/embed/xNMQwgyDOJ0?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="100000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
          />
        </div>
      </div>
      <div class="rubrik tanzen">
        <h2 class="rubrik-title">Zum Tanzen und Lustig-Sein</h2>
        <div class="hörproben-column">
          <Hörprobe
            :playbutton="true"
            title="A night like this"
            musician="Caro Emerald"
            ytLink="https://www.youtube.com/embed/cPW2q7g2fXs?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="85000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
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
          <Hörprobe
            :playbutton="true"
            title="Can’t take my eyes off of you"
            musician="Gloria Gaynor feat. Hermes House Band"
            ytLink="https://www.youtube.com/embed/V6qtLZmjres?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="60000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
          />
          <Hörprobe
            :playbutton="true"
            title="Paradise"
            musician="George Ezra"
            ytLink="https://www.youtube.com/embed/r2bsZF3xl7E?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="65000"
            @clickedOnPlay="handleClickedOnPlay"
            ref="hörprobe"
          />
          <Hörprobe
            :playbutton="true"
            title="Vincent"
            musician="Sarah Connor"
            ytLink="https://www.youtube.com/embed/XS5KUx4xrNU?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="80000"
          />
          <Hörprobe
            :playbutton="true"
            title="Up"
            musician="Olly Murs feat. Demi Lovato"
            ytLink="https://www.youtube.com/embed/y0jfAQ7WeMs?autoplay=1&showinfo=0&controls=0&mute=0"
            timeout="80000"
          />
        </div>
      </div>
      <div class="rubrik haut">
        <h2 class="rubrik-title">Zum "Aus-Der-Haut-Fahren"</h2>
        <div class="hörproben-column">
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
          <Hörprobe
            :playbutton="false"
            title="Rockin all over the world"
            musician="Status Quo"
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
  // methods: {
  //   handleClickedOnPlay(title) {
  //     for (const hörprobe of this.$refs.hörprobe) {
  //       if (hörprobe.title != title) {
  //         hörprobe.handleClickOnPause();
  //       }
  //     }
  //   },
  // },
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

  .hörproben-column {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }
}
</style>
