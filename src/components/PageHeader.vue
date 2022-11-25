<script>
export default {
  name: "PageHeader",
  data() {
    return {
      logoImg: "/src/assets/dc-logo.png",
      links: [
        { label: "characters", href: "#" },
        { label: "comics", href: "#" },
        { label: "movies", href: "#" },
        { label: "tv", href: "#" },
        { label: "games", href: "#" },
        { label: "collectibles", href: "#" },
        { label: "videos", href: "#" },
        { label: "fans", href: "#" },
        { label: "news", href: "#" },
        { label: "shop", href: "#" },
      ],
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
