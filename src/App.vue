<template>
  <div id="nav">
    <div>
      <span>Amazing</span><br />
      {{ projectTitle }}
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
@import url("https://fonts.googleapis.com/css2?family=Inter&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Inter", sans-serif;
}

#nav {
  display: grid;
  place-items: center;
  min-height: 100vh;
  text-align: center;

  span {
    font-size: 1.25rem;
  }
}
</style>
