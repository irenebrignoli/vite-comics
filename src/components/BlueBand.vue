<script>
export default {
  name: "BlueBand",
};
</script>

<template>
  <section id="blue-band"></section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";

#blue-band {
  height: 150px;
  background-color: variables.$primary-color;
}
</style>
