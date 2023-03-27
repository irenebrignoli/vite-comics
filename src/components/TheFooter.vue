<script>
export default {
  name: "TheFooter",
};
</script>

<template>
  <footer>
    <div class="top-footer">
      <div class="container h-100">
        <div class="logo-bg">
          <img src="../assets/dc-logo-bg.png" alt="" />
        </div>
      </div>
    </div>
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

  .container {
    position: relative;
    overflow: hidden;

    .logo-bg {
      position: absolute;
      right: 0;
      top: 50%;
      transform: translateY(-50%);
    }
  }
}

.bottom-footer {
  height: 110px;
  background-color: variables.$footer-bg-color;
}
</style>
