<template>
  <div>
    <img :src="image" :alt="imageSrc" />
    <h2>{{ title }}</h2>
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: "CreateBenefits",
  props: {
    image: String,
    imageSrc: String,
    title: String,
    text: String,
  },
};
</script>

<style scoped>
div {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.25rem;

  text-align: center;
}

h2 {
  color: var(--dark-blue);
  font-size: var(--topic-small);
  font-weight: var(--light);
}

p {
  color: var(--grayish-blue);
}
</style>