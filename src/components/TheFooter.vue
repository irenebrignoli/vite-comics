<script>
export default {
  name: "TheFooter",
};
</script>

<template>
  <footer>
    <div class="top-footer"></div>
    <div class="bottom-footer"></div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";

.top-footer {
  height: 370px;
  background-image: url("../assets/footer-bg.jpg");
  background-size: cover;
  background-position: center;
}

.bottom-footer {
  height: 110px;
  background-color: variables.$footer-bg-color;
}
</style>
