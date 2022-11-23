<template>
  <section class="footer-container">
    <div class="contact-info-container">
      <p class="name">Tanzband Casablanca</p>
      <div class="phone-row">
        <button ref="btn" @click="copyNumberToClipboard">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            v-if="!phoneBtnAlerted"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 24 24"
          >
            <g
              fill="none"
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
            >
              <path
                d="M8 4v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V7.242a2 2 0 0 0-.602-1.43L16.083 2.57A2 2 0 0 0 14.685 2H10a2 2 0 0 0-2 2Z"
              />
              <path
                d="M16 18v2a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V9a2 2 0 0 1 2-2h2"
              />
            </g>
          </svg>
          <svg
            v-else
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 16 16"
          >
            <path
              fill="currentColor"
              d="M12.736 3.97a.733.733 0 0 1 1.047 0c.286.289.29.756.01 1.05L7.88 12.01a.733.733 0 0 1-1.065.02L3.217 8.384a.757.757 0 0 1 0-1.06a.733.733 0 0 1 1.047 0l3.052 3.093l5.4-6.425a.247.247 0 0 1 .02-.022Z"
            />
          </svg>
        </button>
        <p-tel ref="number">+49 152 03419607</p-tel>
      </div>
      <div class="mail-row">
        <button ref="btn" @click="copyMailToClipboard">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            v-if="!mailBtnAlerted"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 24 24"
          >
            <g
              fill="none"
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
            >
              <path
                d="M8 4v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V7.242a2 2 0 0 0-.602-1.43L16.083 2.57A2 2 0 0 0 14.685 2H10a2 2 0 0 0-2 2Z"
              />
              <path
                d="M16 18v2a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V9a2 2 0 0 1 2-2h2"
              />
            </g>
          </svg>
          <svg
            v-else
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 16 16"
          >
            <path
              fill="currentColor"
              d="M12.736 3.97a.733.733 0 0 1 1.047 0c.286.289.29.756.01 1.05L7.88 12.01a.733.733 0 0 1-1.065.02L3.217 8.384a.757.757 0 0 1 0-1.06a.733.733 0 0 1 1.047 0l3.052 3.093l5.4-6.425a.247.247 0 0 1 .02-.022Z"
            />
          </svg>
        </button>
        <p ref="email">info@casablanca-band.com</p>
      </div>
    </div>
  </section>
</template>

<script>
import "../assets/stylesheets/global.scss";
export default {
  data() {
    return {
      phoneBtnAlerted: false,
      mailBtnAlerted: false,
    };
  },
  methods: {
    copyNumberToClipboard() {
      navigator.clipboard.writeText(this.$refs.number.textContent);
      this.phoneBtnAlerted = true;
      setTimeout(() => {
        this.phoneBtnAlerted = false;
      }, 1000);
    },
    copyMailToClipboard() {
      navigator.clipboard.writeText(this.$refs.email.textContent);
      this.mailBtnAlerted = true;
      setTimeout(() => {
        this.mailBtnAlerted = false;
      }, 1000);
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/stylesheets/setup";

.footer-container {
  background-color: $accent-color;
  border-top-left-radius: 2rem;
  border-top-right-radius: 2rem;
  padding: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.contact-info-container {
  background-color: $off-white;
  max-width: 20rem;
  padding: 1rem;
  border-radius: 1rem;
  color: $accent-color;
}

.name {
  margin-bottom: 1rem;
  font-weight: 600;
}

.phone-row {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-weight: 500;
  margin-bottom: 0.25rem;
}
.mail-row {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-weight: 500;
}

button {
  border: none;
  background-color: transparent;
}

svg {
  width: 1.5rem;
  cursor: pointer;
  color: $accent-color;
}
</style>
