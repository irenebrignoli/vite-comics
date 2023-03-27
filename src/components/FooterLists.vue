<script>
export default {
  name: "FooterLists",
  data() {
    return {
      liste: [
        {
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
        {
          title: "Shop",
          links: ["Shop DC", "Shop DC Collectibles"],
        },
        {
          title: "Dc",
          links: [
            "Terms Of Use",
            "Privacy policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "Sites",
          links: [
            "DC",
            "Mad Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
      ],
    };
  },
};
</script>

<template>
  <div class="lists-container">
    <div v-for="(list, index) in liste" class="list-footer">
      <div class="list-title">{{ list.title }}</div>
      <ul v-for="link in list.links" class="list-content">
        <li>{{ link }}</li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";

.lists-container {
  height: 100%;
  margin-top: 50px;
  display: flex;
  gap: 30px;
}
.list-footer {
  display: flex;

  flex-direction: column;
  gap: 10px;
  color: variables.$text-gray-color;
  font-size: 12px;

  .list-title {
    font-size: 16px;
    color: variables.$text-white-color;
    text-transform: uppercase;
  }

  .list-content {
    list-style: none;
  }
}
</style>
