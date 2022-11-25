<script>
import links from "../../assets/jsons/footer-bot-links.json";

export default {
  name: "FooterBot",
  data() {
    return {
      links,
    };
  },
};
</script>

<template>
  <div class="footer-bot">
    <div class="container">
      <button>Sign-Up Now!</button>
      <div class="links">
        <h3><a>Follow Us</a></h3>
        <a v-for="link in links" :href="link.href">
          <img :src="link.image" alt="link.name" />
        </a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.footer-bot {
  background-color: var(--secondary-color);
  padding: 1rem;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  button {
    color: white;
    text-transform: uppercase;
    font-size: 1rem;
    font-weight: 700;
    font-family: inherit;
    background-color: inherit;
    border: 1px solid;
    border-color: var(--blue-color);
    padding: 1rem;
  }
  .links {
    display: flex;
    align-items: center;

    & * {
      line-height: 2rem;
      vertical-align: middle;

      &:not(:last-child) {
        margin-right: 1rem;
      }
    }

    h3 {
      text-transform: uppercase;
      color: var(--blue-color);
    }
  }
}
</style>
