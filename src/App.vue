<script>
import PageHeader from "./components/PageHeader.vue";
import PageMain from "./components/PageMain.vue";
import PageFooter from "./components/PageFooter.vue";

export default {
  components: {
    PageHeader,
    PageMain,
    PageFooter,
  },
};
</script>

<template>
  <div>
    <PageHeader />
    <PageMain />
    <PageFooter />
  </div>
</template>

<style>
@import "./style/global.scss";
</style>
