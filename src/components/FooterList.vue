<script>
export default {
  name: "FooterList",
  props: {
    title: String,
    links: Array,
  },
};
</script>

<template>
  <div class="list">
    <div class="list-title">{{ title }}</div>
    <ul class="list-content">
      <li v-for="(link, i) in links" :key="i">{{ link }}</li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables";

.list {
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

    li {
      padding-bottom: 5px;
    }
  }
}
</style>
