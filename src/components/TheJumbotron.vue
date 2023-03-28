<script>
export default {
  name: "TheJumbotron",
};
</script>

<template>
  <div id="jumbotron">
    <div class="container h-100">
      <div class="series-title">Current Series</div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";
@use "../styles/partials/mixins";

#jumbotron {
  height: 350px;
  background-image: url(../assets/jumbotron.jpg);
  background-size: cover;
  background-position: top;

  .container {
    position: relative;

    .series-title {
      padding: 10px 20px;
      background-color: variables.$primary-color;
      text-transform: uppercase;
      color: variables.$text-white-color;
      display: inline-block;
      font-weight: 700;
      font-size: 18px;
      position: absolute;
      bottom: 0;
      transform: translateY(+50%);
    }
  }
}
</style>
