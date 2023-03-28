<script>
export default {
  name: "SerieCard",
  props: {
    image: String,
    title: String,
  },
};
</script>

<template>
  <div class="card">
    <img :src="image" :alt="title" />
    <div>{{ title }}</div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";
@use "../styles/partials/mixins";

.card {
  color: variables.$text-white-color;
  text-transform: uppercase;
  font-size: 12px;
  font-weight: 500;
  img {
    width: 100%;
    height: 150px;
    object-fit: cover;
    margin-bottom: 8px;
  }
}
</style>
