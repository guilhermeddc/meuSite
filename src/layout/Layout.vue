<template>
  <main>
    <NavBar />
    <slot />
    <ButtonFixed
      :link="links.WhatsApp"
      :image="WhatsApp"
      :alt="alt"
    />
    <Footer />
  </main>
</template>

<script>
import NavBar from '../components/NavBar'
import Footer from '../components/Footer'
import ButtonFixed from '../components/ButtonFixed'
import WhatsApp from "../assets/icons/WhatsApp.png";


export default {
  name: 'Layout',
  components: {
    NavBar,
    Footer,
    ButtonFixed
  },
  data() {
    return {
      WhatsApp,
      alt: " - Guilherme Rodrigues Web Designer, Desenvolvedor Web & Mobile",
      links: {
        WhatsApp: 'https://api.whatsapp.com/send?phone=55055999937833',
      },
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
