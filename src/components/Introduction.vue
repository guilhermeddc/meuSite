<template>
  <section id="introduction">
    <h1>Guilherme Rodrigues</h1>
    <h2>Web Designer, Desenvolvedor Web & Mobile</h2>
    <a class="btn" href="#about">Saiba Mais</a>
  </section>
</template>

<script>
export default {
  name: 'Introduction'
}
</script>

<style lang="scss" scoped>
section {
  background-image: url("../assets/images/concert.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  & h1 {
    color: $light;
    text-shadow: 2px 2px 5px $dark;
    font-weight: 600;
    font-size: 2.9em;
    margin: 20px;
    padding-bottom: 15px;
    padding-top: 15px;
    border-bottom: 4px solid $tertiary;
    border-top: 4px solid $tertiary;
    border-radius: 50px;
    padding-left: 50px;
    padding-right: 50px;
    text-transform: uppercase;
    text-align: center;
  }
  & h2 {
    color: $light;
    text-shadow: 2px 2px 5px $dark;
    font-weight: 400;
    font-size: 2.5em;
    margin-bottom: 30px;
    text-align: center;
  }
  & a {
    color: $light;
    font-weight: 500;
    font-size: 1.1em;
    background: $secondary;
    padding: 15px 60px;
    text-transform: uppercase;
    border-radius: 25px;
    box-shadow: 0 0 2px 1px rgba($color: $tertiary, $alpha: 0.5);
    transition: all 0.3s;
    &:hover {
      opacity: 0.95;
      color: $tertiary;
      box-shadow: 0 0 10px 1px rgba($color: $tertiary, $alpha: 0.5);
    }
  }
}
</style>
