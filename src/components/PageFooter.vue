<script>
import FooterTop from "./footer-components/FooterTop.vue";
import FooterMiddle from "./footer-components/FooterMiddle.vue";
import FooterBot from "./footer-components/FooterBot.vue";

export default {
  name: "PageFooter",
  components: {
    FooterTop,
    FooterMiddle,
    FooterBot,
  },
};
</script>

<template>
  <footer>
    <FooterTop />
    <FooterMiddle />
    <FooterBot />
  </footer>
</template>

<style lang="scss" scoped></style>
