<template>
  <button type="button">{{ text }}</button>
</template>

<script>
export default {
  props: {
    text: String,
  },
};
</script>

<style scoped>
button {
  border-style: none;
  border-radius: 22px;

  padding: 14px 34px;

  background-image: var(--green-gradient);

  color: white;
  font-weight: var(--bold);
}
</style>