<script>
import items from "../../assets/jsons/footer-top-items.json";

export default {
  name: "FooterTop",
  data() {
    return {
      items,
    };
  },
};
</script>

<template>
  <div class="footer-top">
    <div class="container">
      <div v-for="item in items" class="card">
        <a :href="item.href"><img :src="item.image" /></a>
        <a :href="item.href">{{ item.title }}</a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.footer-top {
  background-color: var(--blue-color);
  padding: 1rem;
  .container {
    display: flex;
    justify-content: space-between;
  }
  .card {
    display: flex;
    align-items: center;
    color: white;

    img {
      height: 100px;
    }
    &:last-child img {
      height: 75px;
    }
    a {
      text-transform: uppercase;
      margin-left: 0.5rem;
    }
  }
}
</style>
