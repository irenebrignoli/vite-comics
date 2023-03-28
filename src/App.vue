<script>
import TheHeader from "./components/TheHeader.vue";
import BlueBand from "./components/BlueBand.vue";
import TheFooter from "./components/TheFooter.vue";
import TheJumbotron from "./components/TheJumbotron.vue";
import MainSeries from "./components/MainSeries.vue";
import "@fontsource/open-sans/400.css";
import "@fontsource/open-sans/500.css";
import "@fontsource/open-sans/600.css";
import "@fontsource/open-sans/700.css";

export default {
  data() {
    return {
      BlueList: [
        {
          image: "comics-digital-comics.png",
          name: "Digital Comics",
        },
        {
          image: "comics-merchandise.png",
          name: "Dc Merchandise",
        },
        {
          image: "comics-subscriptions.png",
          name: "Subscription",
        },
        {
          image: "comics-shop-locator.png",
          name: "Comic Shop Locator",
        },
        {
          image: "dc-power-visa.svg",
          name: "Dc Power Visa",
        },
      ],
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
  components: {
    TheHeader,
    BlueBand,
    TheFooter,
    TheJumbotron,
    MainSeries,
  },
};
</script>

<template>
  <TheHeader :title="DcComicsList.title" :links="DcComicsList.links" />
  <TheJumbotron />
  <MainSeries />
  <BlueBand :elements="BlueList" />
  <TheFooter :title="DcComicsList.title" :links="DcComicsList.links" />
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/partials/mixins";
</style>
