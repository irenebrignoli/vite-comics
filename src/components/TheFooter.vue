<script>
import FooterLists from "./FooterLists.vue";
import ListDcComics from "./ListDcComics.vue";

export default {
  name: "TheFooter",
  components: {
    FooterLists,
    ListDcComics,
  },
};
</script>

<template>
  <footer>
    <div class="top-footer">
      <div class="container h-100">
        <FooterLists />
        <div class="logo-bg">
          <img src="../assets/dc-logo-bg.png" alt="" />
        </div>
      </div>
    </div>
    <div class="bottom-footer">
      <div class="container h-100">
        <button>Sign-up now!</button>
        <div class="folow-us">
          <span>Follow Us</span>
          <div class="icons"></div>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";
@use "../styles/partials/mixins";

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

  .container {
    @include mixins.d-flex-center;
    justify-content: space-between;
  }
}
</style>
