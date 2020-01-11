<template>
  <header class="navbar">
    <div class="container">
      <div class="nav">
        <a href="#introduction">
          <img class="logo" :src="Logo" :alt="`Logo ${alt}`" />
        </a>
        <a class="menu" @click="active = !active"><img :src="Menu" :alt="`Menu ${alt}`"></a>
        <nav :class="active ? 'nav-responsive active' : 'nav-responsive'">
          <ul class="nav-links">
            <li>
              <a class="link" href="#services">SERVIÇOS</a>
            </li>
            <li>
              <a class="link" href="#portfolio">PORTIFÓLIO</a>
            </li>
            <li>
              <a class="link" href="#about">SOBRE MIM</a>
            </li>
            <li>
              <a class="link" href="#contact">CONTATO</a>
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
import Menu from "../assets/icons/Menu.png";

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
      Menu,
      active: false,
      alt: " - Guilherme Rodrigues Web Designer, Desenvolvedor Web & Mobile",
      links: {
        Facebook: 'https://www.facebook.com/Guilhermeddc',
        GitHub: 'https://github.com/guilhermeddc',
        Instagram: 'https://www.instagram.com/guilhermeddc/',
        Linkedin: 'https://www.linkedin.com/in/guilhermeddc/',
        WhatsApp: 'https://api.whatsapp.com/send?phone=55055999937833',
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: $tertiary;
  box-shadow: 0 0 5px 3px rgba($color: $dark, $alpha: 0.5);
  transition: all 0.3s;
  & .menu {
    display: none;
    width: 64px;
    padding: 10px;
    cursor: pointer;
    transition: all 0.3s;
  }
  & .nav-responsive {
    display: flex;
    justify-content: space-between;
    width: 100%;
    align-items: center;
    transition: all 0.3s;
  }
  & .nav {
    display: flex;
    align-items: center;
    transition: all 0.3s;
  }
  & .logo {
    height: 60px;
    margin: 10px;
  }
  & .nav-links {
    margin-left: 20px;
    display: flex;
    transition: all 0.3s;
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
  & .nav-social {
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
}
@media screen and (max-width: 992px) {
  .navbar {
    & .menu {
      display: block;
      transition: all 0.3s;
    }
    & .nav {
      justify-content: space-between;
      transition: all 0.3s;
    }
    & .nav-responsive.active {
      display: flex;
      transition: all 0.3s;
    }
    & .nav-responsive {
      display: none;
      position: fixed;
      top: 80px;
      padding: 20px;
      right: 0;
      left: 0;
      height: 250px;
      width: 100%;
      align-items: flex-end;
      background: $tertiary;
      flex-direction: column;
      box-shadow: 0 0 5px 3px rgba($color: $dark, $alpha: 0.5);
      transition: all 0.3s;
    }
    & .nav-links {
      flex-direction: column;
      align-items: flex-end;
      justify-content: space-between;
      transition: all 0.3s;
      & .link {
        display: block;
        padding: 5px 0;
      }
    }
  }
}
@media screen and (max-width: 762px) {
  .navbar {
    & .menu {
      width: 55px;
      display: block;
      transition: all 0.3s;
    }
    & .logo {
      height: 50px;
      margin: 10px;
    }
    & .nav-responsive {
      top: 70px;
    }
  }
}
</style>
