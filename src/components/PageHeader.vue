<script>
import links from "../assets/jsons/header-navbar-links.json";

export default {
  name: "PageHeader",
  data() {
    return {
      logoImg: "/src/assets/img/dc-logo.png",
      links,
    };
  },
};
</script>

<template>
  <header>
    <div class="container">
      <img :src="logoImg" alt="Logo" />
      <ul>
        <li v-for="link in links">
          <a :href="link.href">{{ link.label }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  padding: 1rem;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  ul {
    display: flex;

    li {
      padding: 0.5rem;
    }

    a {
      text-transform: uppercase;
      font-weight: bold;
    }
  }
}
</style>
