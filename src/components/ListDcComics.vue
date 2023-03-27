<script>
export default {
  name: "ListDcComics",
  data() {
    return {
      DcComics: [
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
  <ul>
    <li v-for="item in DcComics">{{ item }}</li>
  </ul>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";

ul {
  display: flex;
  list-style: none;
}
</style>
