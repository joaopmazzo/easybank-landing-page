<template>
  <section class="intro-section">
    <div class="content">
      <h1>Next generation digital banking</h1>
      <p>
        Take your financial life online. Your Easybank account will be a
        one-stop-shop for spending, saving, budgeting, investing, and much more.
      </p>
      <button-component text="Request Invite" />
    </div>
    <img class="image-mockups" :src="imageMockups" :alt="imageMockupsAlt" />
  </section>
</template>

<script>
import Button from "./CreateButton.vue";
import cellphoneMockup from "../assets/image-mockups.png";

export default {
  components: {
    "button-component": Button,
  },
  data() {
    return {
      imageMockups: cellphoneMockup,
      imageMockupsAlt: "image mockups with 4 cellphone",
    };
  },
};
</script>

<style scoped>
.intro-section {
  background: url("../assets/bg-intro-mobile.svg") top no-repeat;

  display: flex;
  flex-direction: column-reverse;
  align-items: center;
  gap: 2.5rem;
}

.image-mockups {
  width: 325px;
  transform: translateY(-8%);
}

.content {
  margin: 0 auto;

  display: flex;
  flex-direction: column;
  align-items: center;
  width: 90%;
}

.content {
  text-align: center;
  margin-bottom: 5.5rem;
}
.content > h1 {
  color: var(--dark-blue);
  font-size: var(--small-header);
  font-weight: var(--light);
}

.content > p {
  margin: 1rem 0 2rem 0;
  color: var(--grayish-blue);
  line-height: 1.563rem;
}
</style>