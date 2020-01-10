<template>
  <main>
    <NavBar />
    <slot />
  </main>
</template>

<script>
import NavBar from '../components/NavBar'

export default {
  name: 'Layout',
  components: {
    NavBar
  }
}
</script>

<style lang="scss" scoped>

</style>
