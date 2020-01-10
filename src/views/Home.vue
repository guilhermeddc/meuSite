<template>
  <Layout>
    <Introduction />
    <Services />
  </Layout>
</template>

<script>
import Layout from '../layout/Layout'
import Introduction from '../components/Introduction'
import Services from '../components/Services'

export default {
  name: 'home',
  components: {
    Layout,
    Introduction,
    Services
  }
}
</script>
