<template>
  <span :style="{ 'font-size': `${size}px` }" class="material-icons">{{
    name
  }}</span>
</template>

<script>
export default {
  props: {
    size: {
      type: String,
      default: "16",
    },
    name: {
      type: String,
      required: true,
    },
  },
  name: "VIcon",
};
</script>
