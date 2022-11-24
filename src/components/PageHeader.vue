<script>
export default {
  name: "PageHeader",
  data() {
    return {
      links: [
        "characters",
        "comics",
        "movies",
        "tv",
        "games",
        "collectibles",
        "videos",
        "fans",
        "news",
        "shop",
      ],
    };
  },
};
</script>

<template>
  <header>
    <div class="container">
      <img src="../assets/dc-logo.png" alt="Logo" />
      <ul>
        <li v-for="link in links">
          <a href="">{{ link }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style scoped>
header {
  padding: 1rem;
}
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
ul {
  display: flex;
  list-style: none;
}
li {
  padding: 0.5rem;
}
a {
  text-transform: uppercase;
  font-weight: bold;
  text-decoration: none;
  color: inherit;
}
</style>
