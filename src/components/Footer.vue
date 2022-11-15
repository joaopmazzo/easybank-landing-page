<template>
  <footer>
    <img class="logo" :src="easybankLogoWhite" alt="EasybakLogo" />
    <div class="social-network">
      <img
        v-for="socialNetworkIcon in socialNetworkIcons"
        :key="socialNetworkIcon.imageSrc"
        :src="socialNetworkIcon.imageSrc"
        :alt="socialNetworkIcon.imageAlt"
      />
    </div>
    <div class="footer-nav">
      <a href="">About Us</a>
      <a href="">Contact</a>
      <a href="">Blog</a>
      <a href="">Careers</a>
      <a href="">Support</a>
      <a href="">Privacy Policy</a>
    </div>
    <button-component text="Request Invite" />
    <span class="copyright">&copy; Easybank. All Rights Reserved</span>
  </footer>
</template>

<script>
import Button from "./CreateButton.vue";

import EasybankLogoWhite from "../assets/logo-white.svg";
import FacebookIcon from "../assets/icon-facebook.svg";
import YoutubeIcon from "../assets/icon-youtube.svg";
import TwitterIcon from "../assets/icon-twitter.svg";
import PinterestIcon from "../assets/icon-pinterest.svg";
import InstagramIcon from "../assets/icon-instagram.svg";

export default {
  name: "Fotter",
  components: {
    "button-component": Button,
  },
  data() {
    return {
      easybankLogoWhite: EasybankLogoWhite,
      socialNetworkIcons: [
        {
          imageSrc: FacebookIcon,
          imageAlt: "Facebook icon",
        },
        {
          imageSrc: YoutubeIcon,
          imageAlt: "Youtube icon",
        },
        {
          imageSrc: TwitterIcon,
          imageAlt: "Twitter icon",
        },
        {
          imageSrc: PinterestIcon,
          imageAlt: "Pinterest icon",
        },
        {
          imageSrc: InstagramIcon,
          imageAlt: "Instagram icon",
        },
      ],
    };
  },
};
</script>

<style>
footer {
  background-color: var(--dark-blue);

  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;

  padding: 2.5rem 0;
}

.logo {
  fill: #fff;
}

.social-network {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.footer-nav {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
}

.footer-nav > a {
  color: var(--white);
  font-size: var(--footer);
}

.copyright {
  color: var(--white);
  font-size: var(--footer);
  opacity: 0.5;
}
</style>