<template>
  <footer>
    <nav>
      <ul class="nav-social">
          <li>
            <a :href="links.Facebook" target="_blank" rel="”noopener”">
              <img :src="Facebook" :alt="`Facebook ${alt}`" />
            </a>
          </li>
          <li>
            <a :href="links.Instagram" target="_blank" rel="”noopener”">
              <img :src="Instagram" :alt="`Instagram ${alt}`" />
            </a>
          </li>
          <li>
            <a :href="links.GitHub" target="_blank" rel="”noopener”">
              <img :src="GitHub" :alt="`GitHub ${alt}`" />
            </a>
          </li>
          <li>
            <a :href="links.Linkedin" target="_blank" rel="”noopener”">
              <img :src="Linkedin" :alt="`Linkedin ${alt}`" />
            </a>
          </li>
          <li>
            <a :href="links.WhatsApp" target="_blank" rel="”noopener”">
              <img :src="WhatsApp" :alt="`WhatsApp ${alt}`" />
            </a>
          </li>
        </ul>
    </nav>
    <div class="copy">
      <p>© 2020 Copyright: Guilherme Rodrigues</p>
    </div>
  </footer>
</template>

<script>
import Logo from "../assets/images/gr-logo-white.png";
import Facebook from "../assets/icons/Facebook.png";
import GitHub from "../assets/icons/GitHub.png";
import Instagram from "../assets/icons/Instagram.png";
import Linkedin from "../assets/icons/Linkedin.png";
import WhatsApp from "../assets/icons/WhatsApp.png";

export default {
  name: 'Footer',
  data() {
    return {
      Logo,
      Facebook,
      GitHub,
      Instagram,
      Linkedin,
      WhatsApp,
      alt: " - Guilherme Rodrigues Web Designer, Desenvolvedor Web & Mobile",
      links: {
        Facebook: 'https://www.facebook.com/Guilhermeddc',
        GitHub: 'https://github.com/guilhermeddc',
        Instagram: 'https://www.instagram.com/guilhermeddc/',
        Linkedin: 'https://www.linkedin.com/in/guilhermeddc/',
        WhatsApp: 'https://api.whatsapp.com/send?phone=55055999937833',
      },
      className: 'navbar',
      teste: window.pageYOffset,
    };
  },
}
</script>

<style lang="scss" scoped>
footer {
  background: $secondary;
  & .nav-social {
    display: flex;
    justify-content: center;
    padding: 50px;
    & li a img {
      width: 50px;
      padding: 5px;
      margin: 10px;
      background: $primary;
      border-left: 2px solid $light;
      border-radius: 25px;
      box-shadow: 0 0 2px 1px rgba($color: $dark, $alpha: 0.12);
      transition: all 0.3s;
      &:hover {
        opacity: 0.7;
        box-shadow: 0 0 5px 3px rgba($color: $dark, $alpha: 0.12);
      }
    }
  }
  & .copy {
    text-align: center;
    background: $tertiary;
    color: $light;
    padding: 20px;
  }
}
</style>