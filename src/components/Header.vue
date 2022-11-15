<template>
  <header>
    <div class="mobile-wrapper">
      <img class="logo" :src="easybankLogoBlack" alt="Easybank logo" />
      <img class="menu" :src="hamburgIcon" alt="menu" @click="toggleMenu" />
    </div>

    <navigation v-show="isMenuOpen" @close="closeMenu" />
    <button-component v-show="showButton" text="Request Invite" />
  </header>
</template>

<script>
import CreateNavigation from "./CreateNavigation.vue";
import Button from "./CreateButton.vue";

import LogoBlack from "../assets/logo-black.svg";
import HamburgIcon from "../assets/icon-hamburger.svg";

export default {
  name: "Header",
  data() {
    return {
      easybankLogoBlack: LogoBlack,
      hamburgIcon: HamburgIcon,
      isMenuOpen: window.innerWidth < 768 ? false : true,
      showButton: window.innerWidth < 768 ? false : true,
    };
  },
  components: {
    navigation: CreateNavigation,
    "button-component": Button,
  },
  methods: {
    onResize() {
      let windowWidth = window.innerWidth;

      this.isMenuOpen = windowWidth < 768 ? false : true;
      this.showButton = windowWidth < 768 ? false : true;
    },
    toggleMenu: function () {
      this.isMenuOpen = !this.isMenuOpen;
    },
    closeMenu: function () {
      this.isMenuOpen = false;
    },
  },
  mounted() {
    this.$nextTick(() => {
      window.addEventListener("resize", this.onResize);
    });
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.onResize);
  },
};
</script>

<style>
header {
  position: fixed;

  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;

  width: 100vw;

  z-index: 99999;
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

@media (min-width: 768px) {
  header {
    flex-direction: row;

    background-color: white;

    padding: 1.125rem;
  }

  .mobile-wrapper {
    width: fit-content;

    padding: 0;
  }

  .menu {
    display: none;
  }

  .button-request {
    display: block;
  }
}
</style>