<template>
  <button class="btn" :class="[`btn-${color}`, `btn-${size}`]">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "v-button",
  props: {
    color: {
      type: String,
      default: "white",
    },
    size: {
      type: String,
      default: "md",
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/imports";

.btn {
  letter-spacing: 0.02em;
  border-radius: 20px;
  font-size: 13px;
  display: flex;
  align-items: center;
  column-gap: 5px;
  padding: 7px;
  border: none;
  font-size: 15px;

  &-yellow {
    background-color: $second;
    border: none;

    &:hover {
      background-color: $hoverYellow;
    }
  }

  &-white {
    border: solid 1px $greyHover;
    background: none;

    &:hover {
      border-color: $grey;
    }
  }

  &-songDarkGrey {
    border: none;
    background: none;
    color: $spanGrey;

    &:hover {
      color: black;
    }
  }

  &-playerGrey {
    border: none;
    background: none;
    color: $grey;

    &:hover {
      color: $buttonHoverBlack;
    }
  }

  &-md {
    height: 40px;
  }
}
</style>
