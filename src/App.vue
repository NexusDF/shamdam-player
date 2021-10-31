<template>
  <div class="container">
    <div class="header">
      <div class="header__logo">
        <VIcon name="music_note" size="32" />
        <span class="header__title">ShamDam Player</span>
      </div>
    </div>
    <div class="wrapper"></div>
    <div class="player-controller">
      <button class="player-controller__prev">
        <VIcon name="fast_rewind" size="28" />
      </button>
      <button class="player-controller__play">
        <VIcon name="play_arrow" size="28" />
      </button>
      <button class="player-controller__next">
        <VIcon name="fast_forward" size="28" />
      </button>
      <button class="player-controller__queue">
        <VIcon name="queue_music" size="28" />
      </button>
      <button class="player-controller__mute">
        <VIcon name="volume_up" size="28" />
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projectTitle: "ShamDam Player",
    };
  },
};
</script>

<style lang="scss">
@import "./scss/imports";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: $backgroundColor;
  font-family: "Inter", sans-serif;
  min-height: 100vh;
  width: 100%;
}

.container {
  background-color: $primary;
  min-height: 100vh;
  width: 1140px;
  display: flex;
  margin: 0 auto;
  position: relative;
}

.header {
  width: 100%;
  height: 70px;
  color: $fontColor;
  border-bottom: solid 1px $borderColor;
  padding: 12px;

  &__logo {
    display: flex;
    align-items: center;
    height: 100%;
    gap: 6px;
  }

  &__title {
    font-size: 1.2rem;
  }
}

.player-controller {
  position: fixed;
  height: 70px;
  bottom: 0;
  max-width: 1140px;
  width: 100%;
  margin: 0 auto;
  border-top: solid 10px $borderColor;
  display: flex;
  align-items: center;

  &__mute {
    margin-left: auto;
  }

  button {
    border: none;
    background-color: transparent;
    padding: 12px;
    color: $grey;
  }

  button:hover {
    color: #123;
  }
}
</style>
