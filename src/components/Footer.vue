<template>
  <footer>
    <div class="wrapper">
      <div class="nav">
        <div class="footer-brand-logos">
          <img :src="easybankLogoWhite" alt="EasybakLogo" />
          <div class="social-network">
            <img v-for="socialNetworkIcon in socialNetworkIcons" :key="socialNetworkIcon.imageSrc"
              :src="socialNetworkIcon.imageSrc" :alt="socialNetworkIcon.imageAlt" />
          </div>
        </div>
        <div class="footer-nav">
          <a href="">About Us</a>
          <a href="">Contact</a>
          <a href="">Blog</a>
          <a href="">Careers</a>
          <a href="">Support</a>
          <a href="">Privacy Policy</a>
        </div>
      </div>
      <div class="button">
        <button-component text="Request Invite" />
        <span class="copyright">&copy; Easybank. All Rights Reserved</span>
      </div>
    </div>
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

<style scoped>
footer {
  background-color: var(--dark-blue);

  padding: 2.5rem 0;
}

.wrapper {
  width: 90%;
  margin: 0 auto;

  display: flex;
  align-items: center;
  flex-wrap: wrap;
  gap: 2rem;
}

.button {
  margin: 0 auto;

  display: flex;
  flex-direction: column;
  align-items: center;

  gap: 2rem;
}

.nav {
  margin: 0 auto;

  display: flex;
  flex-direction: column;
  align-items: center;

  gap: 2rem
}

.footer-brand-logos {
  display: flex;
  flex-direction: column;
  align-items: center;

  gap: 2rem;
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

.footer-nav>a {
  color: var(--white);
  font-size: var(--footer);
}

.copyright {
  color: var(--white);
  font-size: var(--footer);
  opacity: 0.5;
}

@media (min-width: 768px) {
  footer {
    height: 200px;
    padding: 3rem;
  }

  .wrapper {
    max-width: 69.375rem;
    width: 100%;
    height: 100%;

    justify-content: space-between;
  }

  .button {
    margin: 0;
  }

  .nav {
    margin: 0;

    flex-wrap: wrap;
    height: 100%;
  }

  .footer-brand-logos {
    height: 100%;
    justify-content: space-between;
  }

  .footer-nav {
    flex-wrap: wrap;

    height: 100%;
  }

  .copyright {
    height: 100%;
    justify-content: space-between;
  }
}
</style>