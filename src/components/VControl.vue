<template>
  <div class="player-controller">
    <v-button color="playerGrey">
      <VIcon name="fast_rewind" size="28" />
    </v-button>
    <v-button color="playerGrey">
      <VIcon name="play_arrow" size="28" />
    </v-button>
    <v-button color="playerGrey">
      <VIcon name="fast_forward" size="28" />
    </v-button>
    <v-button class="player-controller__queue" color="playerGrey">
      <VIcon name="queue_music" size="28" />
    </v-button>
    <v-button color="playerGrey">
      <VIcon name="volume_up" size="28" />
    </v-button>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../scss/imports";

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
  column-gap: 8px;

  &__queue {
    margin-left: auto;
  }
}
</style>
