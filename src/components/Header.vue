<template>
  <header class="container">
    <div class="mobile-wrapper">
      <img src="../assets/logo.svg" alt="Easybank logo" />
      <img
        class="menu"
        src="../assets/icon-hamburger.svg"
        alt="menu"
        @click="toggleMenu"
      />
    </div>

    <navigation v-show="isMenuOpen" @close="closeMenu" />
    <button class="button-request" type="button">Request Invite</button>
  </header>
</template>

<script>
import CreateNavigation from "./CreateNavigation.vue";
export default {
  name: "Header",
  data() {
    return {
      isMenuOpen: false,
    };
  },
  components: {
    navigation: CreateNavigation,
  },
  methods: {
    toggleMenu: function () {
      this.isMenuOpen = !this.isMenuOpen;
    },
    closeMenu: function () {
      this.isMenuOpen = false;
    },
  },
};
</script>

<style scoped>
header {
  position: fixed;

  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;

  max-width: 1110px;

  z-index: 2;
}

.mobile-wrapper {
  width: 100%;
  padding: 1.375rem;

  display: flex;
  justify-content: space-between;
  align-items: center;

  background-color: white;
}

.button-request {
  display: none;
}

.menu {
  cursor: pointer;
  height: 11px;
}
</style>