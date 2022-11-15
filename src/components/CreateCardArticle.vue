<template>
  <div class="card">
    <img :src="imageSrc" :alt="imageAlt" />
    <div class="card-body">
      <p class="author">{{ author }}</p>
      <h2 class="title">{{ title }}</h2>
      <p class="text">{{ text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CreateCardArticle",
  props: {
    imageSrc: String,
    imageAlt: String,
    author: String,
    title: String,
    text: String,
  },
};
</script>

<style scoped>
.card {
  width: 20.438rem;
  height: 24.688rem;

  display: flex;
  flex-direction: column;
  align-items: flex-start;

  border-radius: 5px;
  overflow: hidden;
  background-color: white;
}

img {
  width: 20.438rem;
  height: 12.5rem;
}

.card-body {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;

  padding: 1.563rem 2rem;
}

.author {
  color: var(--grayish-blue);
  font-size: var(--article-author);
}

.title {
  color: var(--dark-blue);
  font-size: var(--article-title);
  font-weight: var(--light);
  line-height: 1.25rem;
  letter-spacing: -0.013rem;
}

.text {
  color: var(--grayish-blue);
  font-size: var(--article-body);
  line-height: 1.125rem;
  letter-spacing: -0.013rem;
}

@media (min-width: 768px) {
  .card {
    width: 255px;
  }

  .card-body {
    padding: 1.5rem 1.5rem;
  }
}
</style>
