<template>
  <Layout>
    <Introduction />
    <Services />
    <Portfolio />
    <Costumer />
    <About />
    <Contact />
  </Layout>
</template>

<script>
import Layout from '../layout/Layout'
import Introduction from '../components/Introduction'
import Services from '../components/Services'
import Portfolio from '../components/Portfolio'
import Costumer from '../components/Costumer'
import About from '../components/About'
import Contact from '../components/Contact'

export default {
  name: 'home',
  components: {
    Layout,
    Introduction,
    Services,
    Portfolio,
    Costumer,
    About,
    Contact,
  }
}
</script>
