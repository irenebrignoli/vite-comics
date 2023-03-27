<script>
export default {
  name: "TheHeader",
};
</script>

<template>
  <header>
    <div class="container"></div>
  </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";

header {
  height: 110px;
  background-color: variables.$header-bg-color;
}
</style>
