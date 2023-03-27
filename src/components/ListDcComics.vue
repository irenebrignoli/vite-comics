<script>
export default {
  name: "ListDcComics",
  data() {
    return {
      DcComics: {
        title: "DcComics",
        links: [
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
      },
    };
  },
};
</script>

<template>
  <ul>
    <li v-for="link in DcComics.links">{{ link }}</li>
  </ul>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";

ul {
  list-style: none;
}
</style>
