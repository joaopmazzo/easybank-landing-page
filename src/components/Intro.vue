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
    <img
      class="image-mockups-mobile"
      :src="imageMockups"
      :alt="imageMockupsAlt"
    />
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
  background: url("../assets/bg-intro-mobile.svg") var(--very-light-gray) top
    no-repeat;

  display: flex;
  flex-direction: column-reverse;
  align-items: center;
  gap: 2.5rem;
}

.image-mockups-mobile {
  width: 325px;
  transform: translateY(-8%);
}

.content {
  margin: 0 auto;

  display: flex;
  flex-direction: column;
  align-items: center;
  width: 90%;

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
  font-size: var(--content-text-mobile);
  line-height: 1.563rem;
}

@media (min-width: 768px) {
  .intro-section {
    height: 100vh;
    background: url("../assets/bg-intro-desktop.svg") var(--very-light-gray)
      42vw -180px no-repeat;

    flex-direction: row;
  }

  .image-mockups-mobile {
    width: 732px;
    transform: translateY(3%) translateX(15%);
  }

  .content {
    margin: 0 auto;
    width: 27.938rem;

    text-align: start;
    align-items: flex-start;
  }

  .content > h1 {
    font-size: var(--big-header);
  }

  .content > p {
    margin: 1.5rem 0 2.25rem 0;
    font-size: var(--content-text-desktop);
  }
}
</style>