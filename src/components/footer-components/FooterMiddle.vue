<script>
export default {
  name: "FooterMiddle",
  data() {
    return {
      backgroundImage: "/src/assets/footer-bg.jpg",
      logoImageBg: "/src/assets/dc-logo-bg.png",
      lists: [
        {
          title: "DC Comics",
          links: [
            { label: "Characters", href: "#" },
            { label: "Comics", href: "#" },
            { label: "Movies", href: "#" },
            { label: "TV", href: "#" },
            { label: "Games", href: "#" },
            { label: "Videos", href: "#" },
            { label: "News", href: "#" },
          ],
        },
        {
          title: "Shop",
          links: [
            { label: "Shop DC", href: "#" },
            { label: "Shop DC Collectibles", href: "#" },
          ],
        },
        {
          title: "DC",
          links: [
            { label: "Terms Of Use", href: "#" },
            { label: "Privacy Policy", href: "#" },
            { label: "Ad Choices", href: "#" },
            { label: "Advertising", href: "#" },
            { label: "Jobs", href: "#" },
            { label: "Subscriptions", href: "#" },
            { label: "Talent Workshops", href: "#" },
            { label: "CPSC Certificates", href: "#" },
            { label: "Ratings", href: "#" },
            { label: "Shop Help", href: "#" },
            { label: "Contact Us", href: "#" },
          ],
        },
        {
          title: "Sites",
          links: [
            { label: "DC", href: "#" },
            { label: "MAD Magazine", href: "#" },
            { label: "DC Kids", href: "#" },
            { label: "DC Universe", href: "#" },
            { label: "DC Power Visa", href: "#" },
          ],
        },
      ],
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
