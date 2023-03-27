<script>
export default {
  name: "TheHeader",
  data() {
    return {
      headerNavList: [
        "Characters",
        "Comics",
        "Movies",
        "Tv",
        "Games",
        "Collectibles",
        "Videos",
        "Fans",
        "News",
        "Shop",
      ],
    };
  },
};
</script>

<template>
  <header>
    <div class="container h-100">
      <div class="logo h-100">
        <img class="h-100" src="../assets/dc-logo.png" alt="logo DC" />
      </div>
      <nav class="nav-bar">
        <ul>
          <li v-for="item in headerNavList">{{ item }}</li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";
@use "../styles/partials/mixins";

header {
  height: 110px;
  padding: 20px;
  background-color: variables.$header-bg-color;

  .container {
    @include mixins.d-flex-center;
    justify-content: space-between;
  }
}

.nav-bar {
  ul {
    @include mixins.d-flex-center;
    gap: 15px;
    text-transform: uppercase;
    font-size: 10px;
    list-style: none;
  }
}
</style>
