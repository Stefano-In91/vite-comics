<script>
import lists from "../../assets/jsons/footer-middle-lists.json";

export default {
  name: "FooterMiddle",
  data() {
    return {
      backgroundImage: "/src/assets/img/footer-bg.jpg",
      logoImageBg: "/src/assets/img/dc-logo-bg.png",
      lists,
    };
  },
};
</script>

<template>
  <div
    class="footer-middle"
    :style="`background-image: url(${backgroundImage})`"
  >
    <div class="container">
      <div class="lists">
        <div v-for="list in lists" class="list">
          <h3>{{ list.title }}</h3>
          <ul>
            <li v-for="link in list.links">
              <a :href="link.href">{{ link.label }}</a>
            </li>
          </ul>
        </div>
      </div>
      <img :src="logoImageBg" alt="logo" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.footer-middle {
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 400px;
  overflow: hidden;
  color: white;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
  }
  .lists {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    height: 70%;

    .list {
      margin-right: 1rem;

      h3 {
        margin: 0.5rem 0;
        text-transform: uppercase;
      }
      li a {
        color: gray;
      }
    }
  }
}
</style>
