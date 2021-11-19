<template>
  <header class="header">
    <div class="header__logo">
      <div class="header__inner">
        <VIcon name="music_note" size="32" />
        <span class="header__title">
          <slot></slot>
        </span>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
@import "../scss/imports";
.header {
  display: flex;
  width: 100%;
  color: $fontColor;
  border-bottom: solid 1px $borderColor;
  padding: 15px 12px;

  &__logo {
    transition: all 0.4s ease-in-out;
  }

  &__inner {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  &__title {
    font-size: 1.2rem;
  }
}
@media screen {
  @media (max-width: 768px) {
    .header__logo {
      flex: 1 0 200px;
    }
  }
}
</style>
