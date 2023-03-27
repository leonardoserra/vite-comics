<script>
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
import Banner from "./components/Banner.vue";

export default {
  components: {
    TheHeader,
    TheFooter,
    Banner
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
  <main>

  </main>
  <TheFooter />
  <Banner />
</template>

<style lang="scss">
body {
  // debug
  background-color: aqua;
}
</style>
