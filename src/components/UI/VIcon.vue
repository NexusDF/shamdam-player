<template>
  <span :style="{ 'font-size': `${size || byDef}px` }" class="material-icons">{{
    name
  }}</span>
</template>

<script>
export default {
  props: {
    size: {
      type: String,
    },
    name: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      byDef: "16",
    };
  },
  name: "VIcon",
};
</script>
