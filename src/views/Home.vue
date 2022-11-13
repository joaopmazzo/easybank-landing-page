<template>
  <header-component />
  <intro-section />
  <!-- <div id="container-wrapper"> -->
  <benefits-sections />
  <!-- </div> -->
</template>

<script>
import Header from "../components/Header.vue";
import Intro from "../components/Intro.vue";
import Benefits from "../components/Benefits.vue";

export default {
  name: "Home",
  components: {
    "header-component": Header,
    "intro-section": Intro,
    "benefits-sections": Benefits,
  },
};
</script>

<style>
/* #container-wrapper {
  width: 90%;
  margin: 0 auto;
} */
</style>