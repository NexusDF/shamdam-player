<template>
  <div class="player-controller">
    <v-button color="player-grey">
      <VIcon name="fast_rewind" size="28" />
    </v-button>
    <v-button color="player-grey">
      <VIcon name="play_arrow" size="28" />
    </v-button>
    <v-button color="player-grey">
      <VIcon name="fast_forward" size="28" />
    </v-button>
    <v-button class="player-controller__queue" color="player-grey">
      <VIcon name="queue_music" size="28" />
    </v-button>
    <v-button color="player-grey">
      <VIcon name="volume_up" size="28" />
    </v-button>
  </div>
</template>

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
