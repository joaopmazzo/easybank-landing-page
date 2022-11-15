<template @keydown.esc="close">
  <div id="overlay" @click="outsideClick" @keydown.esc="close">
    <nav>
      <a href="#">Home</a>
      <a href="#">About</a>
      <a href="#">Contact</a>
      <a href="#">Blog</a>
      <a href="#">Careers</a>
    </nav>
  </div>
</template>

<script>
export default {
  name: "CreateNavigation",
  methods: {
    outsideClick: function (e) {
      if (e.target.id === "overlay") {
        this.$emit("close");
      }
    },
    close: function () {
      this.$emit("close");
    },
  },
};
</script>

<style scoped>
#overlay {
  width: 100vw;
  height: calc(100vh - 64px);

  background: var(--overlay);
}

nav {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  gap: 1.5rem;
  padding: 2rem 0;
  margin: 1.5rem;

  background: white;
  border-radius: 4px;

  font-size: var(--navitem-mobile);
}
</style>