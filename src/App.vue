<script>
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
import BannerBottom from "./components/BannerBottom.vue";
import BannerBonus from "./components/BannerBonus.vue";
import TheJumbotron from "./components/TheJumbotron.vue";
import CardSection from "./components/CardSection.vue";

export default {
  components: {
    TheHeader,
    TheFooter,
    BannerBonus,
    BannerBottom,
    TheJumbotron,
    CardSection
  },
  data() {
    return {

    };
  },
  methods: {

  }


};
</script>

<template>
  <TheHeader />
  <TheJumbotron />
  <CardSection />
  <BannerBonus />
  <TheFooter />
  <BannerBottom />
</template>

<style lang="scss">
body {
  // debug
  background-color: black;

  main {
    height: 120px;
    color: white;
  }
}
</style>
