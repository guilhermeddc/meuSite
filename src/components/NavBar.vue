<template>
  <header :class="className" @scroll="teste">
    <div class="container">
      <div class="nav">
        <a href="#introduction">
          <img class="logo" :src="Logo" :alt="`Logo ${alt}`" />
        </a>
        <nav>
          <ul class="nav-links">
            <li>
              <a href="#services">SERVIÇOS</a>
            </li>
            <li>
              <a href="#portfolio">PORTIFÓLIO</a>
            </li>
            <li>
              <a href="#about">SOBRE MIM</a>
            </li>
            <li>
              <a href="#contact">CONTATO</a>
            </li>
          </ul>
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
      </div>
    </div>
  </header>
</template>

<script>
import Logo from "../assets/images/gr-logo-white.png";
import Facebook from "../assets/icons/Facebook.png";
import GitHub from "../assets/icons/GitHub.png";
import Instagram from "../assets/icons/Instagram.png";
import Linkedin from "../assets/icons/Linkedin.png";
import WhatsApp from "../assets/icons/WhatsApp.png";

export default {
  name: "NavBar",
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
  watch: {
    teste(newVal) {
      if (newVal) {
        return this.teste = document.documentElement.scrollTop
      }
    }
  },
  methods: {
    handleScroll() {
      if (window.scrollY > 50) {
        this.className = 'navbarDown'
      }
      return window.scrollY > 100;
    }
  }
};
</script>

<style lang="scss" scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: $tertiary;
  box-shadow: 0 0 5px 3px rgba($color: $dark, $alpha: 0.5)
}
.navbarDown {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: $tertiary;
  box-shadow: 0 0 5px 3px rgba($color: $dark, $alpha: 0.5)
}
nav {
  display: flex;
  justify-content: space-between;
  width: 100%;
  align-items: center;
}
.nav {
  display: flex;
}
.logo {
  height: 60px;
  margin: 10px;
}
.nav-links {
  margin-left: 20px;
  display: flex;
  & li a {
    margin: 7px;
    font-weight: 500;
    font-size: 16px;
    color: $light;
    transition: all 0.3s;
    &:hover {
      opacity: 0.7;
    }
  }
}
.nav-social {
  display: flex;
  & li a img {
    width: 28px;
    margin: 0 10px 0 0;
    transition: all 0.3s;
    &:hover {
      opacity: 0.7;
    }
  }
}
</style>
