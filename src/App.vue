<script>
import TheHeader from "./components/TheHeader.vue";
import BlueBand from "./components/BlueBand.vue";
import TheFooter from "./components/TheFooter.vue";
import "@fontsource/open-sans/400.css";
import "@fontsource/open-sans/500.css";
import "@fontsource/open-sans/600.css";
import "@fontsource/open-sans/700.css";

export default {
  data() {
    return {
      DcComicsList: {
        title: "Dc Comics",
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
  methods: {},
  components: {
    TheHeader,
    BlueBand,
    TheFooter,
  },
};
</script>

<template>
  <TheHeader :title="DcComicsList.title" :links="DcComicsList.links" />
  <div class="debug-main">
    <div class="container">
      <h2>Content main here</h2>
    </div>
  </div>
  <BlueBand />
  <TheFooter :title="DcComicsList.title" :links="DcComicsList.links" />
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/partials/mixins";

.debug-main {
  height: 150px;
  background-color: black;
  color: #fff;
  line-height: 150px;
}
</style>
