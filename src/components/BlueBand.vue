<script>
export default {
  name: "BlueBand",
  props: {
    elements: Array,
  },
  methods: {
    getImageUrl(name) {
      return new URL(`../assets/${name}`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <section id="blue-band">
    <div class="container h-100">
      <div v-for="(element, i) in elements" class="link" :key="i">
        <img :src="getImageUrl(`buy-${element.image}`)" :alt="element.image" />
        <span>{{ element.name }}</span>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";
@use "../styles/partials/mixins";

#blue-band {
  height: 150px;
  background-color: variables.$primary-color;

  .container {
    @include mixins.d-flex-center;
    justify-content: center;
    gap: 60px;

    .link {
      @include mixins.d-flex-center;
      img {
        height: 50px;
        margin-right: 10px;
      }

      span {
        font-size: 12px;
        font-weight: 500;
        color: variables.$text-white-color;
        text-transform: uppercase;
      }

      &:last-child img {
        height: 40px;
      }
    }
  }
}
</style>
