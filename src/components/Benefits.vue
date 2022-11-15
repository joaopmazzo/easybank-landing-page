<template>
  <section>
    <div class="wrapper">
      <div class="section-header">
        <h1>Why choose Easybank?</h1>
        <p>
          We leverage Open Banking to turn your bank account into your financial
          hub. Control your finances like never before.
        </p>
      </div>
      <div class="section-body">
        <create-benefits-component
          v-for="benefit in benefits"
          :key="benefit.title"
          :image="benefit.image"
          :imageSrc="benefit.imageSrc"
          :title="benefit.title"
          :text="benefit.text"
        />
      </div>
    </div>
  </section>
</template>

<script>
import CreateBenefits from "./CreateBenefits.vue";

import OnlineIcon from "../assets/icon-online.svg";
import BudgetingIcon from "../assets/icon-budgeting.svg";
import OnboardingIcon from "../assets/icon-onboarding.svg";
import ApiIcon from "../assets/icon-api.svg";

export default {
  name: "Benefits",
  components: {
    "create-benefits-component": CreateBenefits,
  },
  data() {
    return {
      benefits: [
        {
          image: OnlineIcon,
          imageSrc: "hand with credits cards",
          title: "Online Banking",
          text: "Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world.",
        },
        {
          image: BudgetingIcon,
          imageSrc: "phone with currency icon",
          title: "Simple Budgeting",
          text: "See exactly where your money goes each month. Receive notifications when you're close to your hitting limits",
        },
        {
          image: OnboardingIcon,
          imageSrc: "group of people interacting",
          title: "Fast Onboarding",
          text: "We don't do branches. Open your account in minutes online and start taking control of your finances right away",
        },
        {
          image: ApiIcon,
          imageSrc: "chipset representation",
          title: "Open API",
          text: "Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier.",
        },
      ],
    };
  },
};
</script>

<style scoped>
section {
  padding: 4rem 0;
  background: var(--light-grayish-blue);
}

.wrapper {
  width: 90%;
  margin: 0 auto;
}

.section-header {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.875rem;
  margin-bottom: 3.5rem;

  text-align: center;
}

.section-header > h1 {
  color: var(--dark-blue);
  font-size: var(--section-header-mobile);
  font-weight: var(--light);
}

.section-header > p {
  color: var(--grayish-blue);
}

.section-body {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

@media (min-width: 768px) {
  section {
    padding: 6rem 0;
  }

  .wrapper {
    max-width: 69.375rem;
  }

  .section-header {
    width: 39.688rem;

    align-items: flex-start;
    gap: 1rem;

    text-align: start;
  }

  .section-header > h1 {
    font-size: var(--section-header-desktop);
  }

  .section-header > p {
    font-size: var(--content-text-desktop);
  }

  .section-body {
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }
}
</style>