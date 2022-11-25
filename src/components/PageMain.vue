<script>
import comics from "../assets/jsons/dc-comics.json";

export default {
  name: "PageMain",
  data() {
    return {
      comics,
      currentSeriesImg: "src/assets/jumbotron.jpg",
    };
  },
};
</script>

<template>
  <main>
    <section
      class="current-series"
      :style="`background-image: url(${currentSeriesImg})`"
    >
      <div class="container">
        <div><h3>Current Series</h3></div>
      </div>
    </section>
    <div class="carousel container">Insert shit here</div>
  </main>
</template>

<style lang="scss" scoped>
main {
  .current-series {
    background-size: cover;
    background-repeat: no-repeat;
    height: 21rem;

    .container {
      position: relative;
      height: 100%;

      div {
        color: white;
        background-color: var(--blue-color);
        display: inline-block;
        padding: 0.75rem 1rem;
        position: absolute;
        bottom: -25px;
        left: 0;

        h3 {
          text-transform: uppercase;
        }
      }
    }
    .carousel {
      background-color: var(--primary-color);
    }
  }
}
</style>
