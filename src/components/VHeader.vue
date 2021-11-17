<template>
  <header class="header">
    <div class="header__logo">
      <VIcon name="music_note" size="32" />
      <span class="header__title">
        <slot></slot>
      </span>
    </div>
  </header>
</template>

<style scoped lang="scss">
@import "../scss/imports";
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
</style>
