<template>
  <div class="cta-box">
    <button @click="scrollToBottom" class="cta-btn">AUFTRITT BUCHEN</button>
    <div class="icon-box">
      <a
        href="https://instagram.com/partyband_casablanca?igshid=YmMyMTA2M2Y="
        target="_blank"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          preserveAspectRatio="xMidYMid meet"
          viewBox="0 0 1024 1024"
          class="icon ig-icon"
        >
          <path
            fill="currentColor"
            d="M512 378.7c-73.4 0-133.3 59.9-133.3 133.3S438.6 645.3 512 645.3S645.3 585.4 645.3 512S585.4 378.7 512 378.7zM911.8 512c0-55.2.5-109.9-2.6-165c-3.1-64-17.7-120.8-64.5-167.6c-46.9-46.9-103.6-61.4-167.6-64.5c-55.2-3.1-109.9-2.6-165-2.6c-55.2 0-109.9-.5-165 2.6c-64 3.1-120.8 17.7-167.6 64.5C132.6 226.3 118.1 283 115 347c-3.1 55.2-2.6 109.9-2.6 165s-.5 109.9 2.6 165c3.1 64 17.7 120.8 64.5 167.6c46.9 46.9 103.6 61.4 167.6 64.5c55.2 3.1 109.9 2.6 165 2.6c55.2 0 109.9.5 165-2.6c64-3.1 120.8-17.7 167.6-64.5c46.9-46.9 61.4-103.6 64.5-167.6c3.2-55.1 2.6-109.8 2.6-165zM512 717.1c-113.5 0-205.1-91.6-205.1-205.1S398.5 306.9 512 306.9S717.1 398.5 717.1 512S625.5 717.1 512 717.1zm213.5-370.7c-26.5 0-47.9-21.4-47.9-47.9s21.4-47.9 47.9-47.9s47.9 21.4 47.9 47.9a47.84 47.84 0 0 1-47.9 47.9z"
          />
        </svg>
      </a>
      <a href="https://www.facebook.com/pcasablanca" target="_blank">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          preserveAspectRatio="xMidYMid meet"
          viewBox="0 0 1000 1000"
          class="icon fb-icon"
        >
          <path
            fill="currentColor"
            d="M182.594 0C81.445 0 0 81.445 0 182.594v634.813c0 101.149 81.445 182.594 182.594 182.594h344.063V609.063H423.282v-140.75h103.375v-120.25c0-94.475 61.079-181.219 201.781-181.219c56.968 0 99.094 5.469 99.094 5.469l-3.313 131.438s-42.963-.406-89.844-.406c-50.739 0-58.875 23.378-58.875 62.188v102.781h152.75l-6.656 140.75H675.5v390.938h141.906c101.149 0 182.594-81.445 182.594-182.594V182.595C1000 81.446 918.555.001 817.406.001H182.593z"
          />
        </svg>
      </a>
      <a
        href="https://youtube.com/channel/UCwD7c1ZCx15oWVnJIXy2TiA"
        target="_blank"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          preserveAspectRatio="xMidYMid meet"
          viewBox="0 0 20 20"
          class="icon yt-icon"
        >
          <path
            fill="currentColor"
            d="M11.603 9.833L9.357 8.785C9.161 8.694 9 8.796 9 9.013v1.974c0 .217.161.319.357.228l2.245-1.048c.197-.092.197-.242.001-.334zM10 .4C4.698.4.4 4.698.4 10s4.298 9.6 9.6 9.6s9.6-4.298 9.6-9.6S15.302.4 10 .4zm0 13.5c-4.914 0-5-.443-5-3.9s.086-3.9 5-3.9s5 .443 5 3.9s-.086 3.9-5 3.9z"
          />
        </svg>
      </a>
    </div>
  </div>
</template>

<script>
import "../assets/stylesheets/global.scss";

export default {
  methods: {
    scrollToBottom() {
      window.scrollTo({ top: document.body.scrollHeight, behavior: "smooth" });
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/stylesheets/setup";

.cta-box {
  width: 100%;
  background-color: $accent-color;
  padding-block: 4rem;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2rem;
  border-top-left-radius: 2rem;
  border-top-right-radius: 2rem;

  .cta-btn {
    padding-block: 0.75rem;
    padding-inline: 1rem;
    border: none;
    color: $accent-color;
    background-color: white;
    border-radius: 2rem;
    font-weight: 700;
    cursor: pointer;
    transition: all 300ms ease-in-out;

    &:hover {
      // filter: drop-shadow(0px 0px 20px #fff);
      transform: scale(1.05);
    }

    @media (min-width: $bp-md) {
      padding-block: 1.5em;
      padding-inline: 2rem;
    }
  }

  .icon-box {
    display: flex;
    gap: 0.75rem;
    align-items: center;

    @media (min-width: $bp-md) {
      gap: 2rem;
    }

    .icon {
      color: white;
      transition: all 300ms ease-in-out;

      &:hover {
        transform: scale(1.05);
      }
    }
    .ig-icon {
      width: 2.8rem;
    }
    .fb-icon {
      width: 2rem;
    }
    .yt-icon {
      width: 2.6rem;
    }
  }
}
</style>
