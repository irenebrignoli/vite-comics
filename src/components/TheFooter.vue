<script>
import FooterList from "./FooterList.vue";

export default {
  name: "TheFooter",
  components: {
    FooterList,
  },
  props: {
    title: String,
    links: Array,
  },
  data() {
    return {
      followIcons: ["facebook", "periscope", "pinterest", "twitter", "youtube"],
      listFooter: [
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
  methods: {
    getImageUrl(name) {
      return new URL(`../assets/${name}`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <footer>
    <div class="top-footer">
      <div class="container h-100">
        <div class="lists-container">
          <FooterList :title="title" :links="links" />
          <div v-for="(list, index) in listFooter" :key="index">
            <FooterList :title="list.title" :links="list.links" />
          </div>
        </div>
        <div class="logo-bg">
          <img src="../assets/dc-logo-bg.png" alt="" />
        </div>
      </div>
    </div>
    <div class="bottom-footer">
      <div class="container h-100">
        <button class="my-btn">Sign-up now!</button>
        <div class="follow-us">
          <span>Follow Us</span>
          <div class="icons">
            <img
              v-for="(icon, index) in followIcons"
              :src="getImageUrl(`footer-${icon}.png`)"
              :alt="icon"
              :key="`icon-${index}`"
            />
          </div>
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

    .lists-container {
      height: 100%;
      margin-top: 30px;
      display: flex;
      gap: 30px;
    }
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

    .follow-us {
      @include mixins.d-flex-center;
      gap: 15px;

      span {
        text-transform: uppercase;
        color: variables.$primary-color;
        font-weight: 700;
      }

      .icons img {
        margin-left: 15px;
      }
    }
  }
}
</style>
