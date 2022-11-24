<script>
export default {
  name: "FooterTop",
  data() {
    return {
      items: [
        {
          image: "src/assets/buy-comics-digital-comics.png",
          title: "digital comics",
        },
        {
          image: "src/assets/buy-comics-merchandise.png",
          title: "dc merchandise",
        },
        {
          image: "src/assets/buy-comics-subscriptions.png",
          title: "subscription",
        },
        {
          image: "src/assets/buy-comics-shop-locator.png",
          title: "comic shop locator",
        },
        {
          image: "src/assets/buy-dc-power-visa.svg",
          title: "dc power visa",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="footer-top">
    <div class="container">
      <div v-for="item in items" class="card">
        <a><img :src="item.image" /></a>
        <a>{{ item.title }}</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.footer-top {
  background-color: var(--blue-color);
  padding: 1rem;
}
.container {
  display: flex;
  justify-content: space-between;
  padding: 1rem;
}
.card {
  display: flex;
  align-items: center;
  color: white;
}
img {
  height: 100px;
}
.card:last-child img {
  height: 75px;
}
a {
  text-transform: uppercase;
  margin-left: 0.5rem;
}
</style>
