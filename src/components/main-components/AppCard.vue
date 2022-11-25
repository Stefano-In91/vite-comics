<script>
export default {
  name: "AppCard",
  props: {
    image: "String",
    title: "String",
  },
};
</script>

<template>
  <div class="card">
    <img :src="image" :alt="title" />
    <h4>{{ title }}</h4>
  </div>
</template>

<style lang="scss" scoped>
.card {
  max-width: calc(100% / 12 * 2);
  padding: 1rem;

  img {
    object-fit: cover;
    height: calc(var(--container-max-width) / 12 * 2 - 2rem);
    width: calc(var(--container-max-width) / 12 * 2 - 2rem);
    object-position: top;
  }
  h4 {
    padding: 0.75rem 0;
    text-transform: uppercase;
    color: white;
  }
}
</style>
