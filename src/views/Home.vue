<template>
  <intro-section />
  <!-- <div id="container-wrapper"> -->
  <benefits-sections />
  <articles-section />
  <!-- </div> -->
</template>

<script>
import Intro from "../components/Intro.vue";
import Benefits from "../components/Benefits.vue";
import Articles from "../components/Articles.vue";

export default {
  name: "Home",
  components: {
    "intro-section": Intro,
    "benefits-sections": Benefits,
    "articles-section": Articles,
  },
};
</script>

<style>
</style>