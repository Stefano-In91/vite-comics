<script>
export default {
  name: "FooterMiddle",
  data() {
    return {
      lists: [
        {
          title: "DC Comics",
          links: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          title: "Shop",
          links: ["Shop DC", "Shop DC Collectibles"],
        },
        {
          title: "DC",
          links: [
            "Terms Of Use",
            "Privacy Policy",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "Sites",
          links: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
      ],
    };
  },
};
</script>

<template>
  <div class="footer-middle">
    <div class="container">
      <div class="lists">
        <div v-for="list in lists" class="list">
          <h3>{{ list.title }}</h3>
          <ul>
            <li v-for="link in list.links">
              <a href="">{{ link }}</a>
            </li>
          </ul>
        </div>
      </div>
      <img src="src/assets/dc-logo-bg.png" alt="logo" />
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100%;
}
.footer-middle {
  background-image: url("src/assets/footer-bg.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 400px;
  overflow: hidden;
  color: white;
}
.lists {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  height: 70%;
}
.list {
  margin-right: 1rem;
}
h3 {
  margin: 0.5rem 0;
  text-transform: uppercase;
}
li a {
  color: gray;
}
</style>
