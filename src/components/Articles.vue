<template>
  <section>
    <div class="wrapper">
      <h1>Latest Articles</h1>
      <div class="section-body">
        <create-card-article-component
          v-for="article in articles"
          :key="article.title"
          :imageSrc="article.imageSrc"
          :imageAlt="article.imageAlt"
          :author="article.author"
          :title="article.title"
          :text="article.text"
        />
      </div>
    </div>
  </section>
</template>

<script>
import CreateCardArticle from "./CreateCardArticle.vue";

import CurrencyImage from "../assets/image-currency.jpg";
import RestaurantImage from "../assets/image-restaurant.jpg";
import PlaneImage from "../assets/image-plane.jpg";
import ConfettiImage from "../assets/image-confetti.jpg";

export default {
  name: "Articles",
  data() {
    return {
      articles: [
        {
          imageSrc: CurrencyImage,
          imageAlt: "Currency image",
          author: "By Claire Robinson",
          title: "Receive money in any currency with no fees",
          text: "The world is getting smaller and we're becoming more mobile. So why should you be forced to only receive money in a single...",
        },
        {
          imageSrc: RestaurantImage,
          imageAlt: "Restaurant table image",
          author: "By Wilson Hutton",
          title: "Treat yourself without worrying about money",
          text: "Our simple budgeting feature allows you to separate out your spending and set realistic limits each month, That means you...",
        },
        {
          imageSrc: PlaneImage,
          imageAlt: "Airplane wing image",
          author: "By Wilson Hutton",
          title: "Take your Easybank card wherever you go",
          text: "We want to enjoy your travels. This is why we don't charge any fees on purchases while you're abroad. We'll even show you...",
        },
        {
          imageSrc: ConfettiImage,
          imageAlt: "Confetti image",
          author: "By Claire Robinson",
          title: "Our invite-only Beta accounts are now live!",
          text: "After a lot of hard work by the whole team, we're excited to launch our closed beta. It's easy to request an invite through the site...",
        },
      ],
    };
  },
  components: {
    "create-card-article-component": CreateCardArticle,
  },
};
</script>

<style scoped>
section {
  padding: 5.5rem 0;
  background: var(--very-light-gray);
}

.wrapper {
  width: 90%;
  margin: 0 auto;
}

.wrapper > h1 {
  color: var(--dark-blue);
  font-size: var(--section-header-mobile);
  font-weight: var(--light);
  text-align: center;

  margin-bottom: 1.9375rem;
}

.section-body {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

@media (min-width: 768px) {
  section {
    padding: 5rem 0;
  }

  .wrapper {
    width: 100%;
    max-width: 69.375rem;
  }

  .wrapper > h1 {
    font-size: var(--section-header-desktop);
    text-align: start;

    margin-bottom: 2.5rem;
  }

  .section-body {
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;

    gap: 1.875rem;
  }
}
</style>