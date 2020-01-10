<template>
  <section id="services" class="container">
    <h1 class="services-title">Web Designer, Desenvolvedor Web & Mobile</h1>
    <p class="services-text">Conheça minhas formas de trabalhar!</p>
    <div class="services-content">
      <div class="card">
        <img :src="SmartphoneTablet" alt="">
        <h2>Design Responsivo</h2>
        <p>
          Sites com Design Responsivo que podem serem abertos em qualquer tipo de plataforma, desde celular, tablet e computador pessoal.
        </p>
      </div>
      <div class="card">
        <img :src="Android" alt="">
        <h2>Aplicativos Android e IOS</h2>
        <p>Criar um aplicativo robusto para sua empresa ou negócio, ou iniciar uma novo projeto.</p>
      </div>
      <div class="card">
        <img :src="ShoppingCart" alt="">
        <h2>E-Commerce</h2>
        <p>
          Quer criar e manter seu negócio online? Criamos de forma completa e acessível, e tem a opção de manutenção ou ensinamos a utilizá-lo.
        </p>
      </div>
      <div class="card">
        <img :src="OnlineSupport" alt="">
        <h2>Suporte</h2>
        <p>
          Suporte a erros e bugs que podem acontecer, e suporte para modificações em períodos acertados no momento da contratação.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
import Android from '../assets/icons/Android.png'
import OnlineSupport from '../assets/icons/OnlineSupport.png'
import ShoppingCart from '../assets/icons/ShoppingCart.png'
import SmartphoneTablet from '../assets/icons/SmartphoneTablet.png'

export default {
  name: 'Services',
  data() {
    return {
      Android,
      OnlineSupport,
      ShoppingCart,
      SmartphoneTablet,
    }
  }
}
</script>

<style lang="scss" scoped>
#services {
  padding: 50px 0;
}
.services-title {
  text-align: center;
  padding: 50px 0 20px;
  font-size: 2em;
  text-shadow: 0px 1px 3px $tertiary;
}
.services-text {
  font-style: italic;
  color: $secondary;
  font-weight: 300;
  text-align: center;
  padding: 0 0 50px;
}
.services-content {
  display: flex;
  flex-wrap: wrap;
}
.card {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 5px;
  text-align: center;
  border-radius: 25px;
  color: $light;
  padding: 10px;
  & h2 {
    font-weight: 600;
    padding-bottom: 10px;
  }
  & p {
    font-weight: 300;
    padding-bottom: 10px;
  }
  &:nth-child(1) {
    background: $primary;
  }
  &:nth-child(2) {
    background: $secondary;
  }
  &:nth-child(3) {
    background: $primary;
  }
  &:nth-child(4) {
    background: $secondary;
  }
}
</style>
