<template>
  <section id="about" class="container">
    <h2>SOBRE MIM</h2>
    <p>Conheça minha história de vida.</p>
    <div class="about">
      <img :src="About" alt="">
      <div class="about-info">
        <h3>2013-2015 - Comecei meus estudos</h3>
        <p>
          Na UNIFRA, hoje UFN... Mas por motivos maiores tive que parar, mas o sonho não havia acabado, apenas adiado.
        </p>
        <h3>Agosto 2018 - Início de uma nova fase</h3>
        <p>
          Entrei na Antônio Meneghetti Faculdade e lá redescobri meu sonho e desde então estou engajado a ser o melhor de mim e me realizar na vida profissional.
        </p>
        <h3>Fevereiro 2019 - Inicio dos negócios</h3>
        <p>
          Após muito estudo comecei a vender meus serviços e mostrando meu portifólio para todos os possíveis clientes para tentar erguer minha marca e criar meu valor.
        </p>
        <h3>Março 2019 - Ganhando experiência...</h3>
        <p>
          Consegui completar projetos e adquirir novos e com garra e determinação irei em frente aceitando todos os desafios.
        </p>
        <h3>Novembro 2019 - Novo ciclo iniciado</h3>
        <p>
          Meu primerio emprego em uma empresa da area, trabalhando com diferentes tecnologias e utilizando métodos ágeis.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
import About from '../assets/images/eu.jpg'

export default {
  name: 'About',
  data() {
    return {
      About
    }
  }
}
</script>

<style lang="scss" scoped>
section {
  padding-top: 50px !important;
  padding-bottom: 150px !important;
  & h2 {
    text-align: center;
    color: $dark;
    padding: 50px 0 20px;
    font-size: 2em;
    text-shadow: 0px 1px 3px $dark;
  }
  & > p {
    font-style: italic;
    color: $dark;
    font-weight: 300;
    text-align: center;
    padding: 0 0 50px;
  }
  & .about {
    display: flex;
    & img {
      border-top: 4px solid $primary;
      border-bottom: 4px solid $primary;
      max-width: 360px;
      border-bottom-left-radius: 25px;
      border-top-left-radius: 25px;
      box-shadow: 0.5px 0px 5px 1px rgba(0,0,0,0.3);
    }
    & .about-info {
      border-top: 4px solid $primary;
      border-bottom: 4px solid $primary;
      border-bottom-right-radius: 25px;
      border-top-right-radius: 25px;
      box-shadow: 0.5px 0px 5px 1px rgba(0,0,0,0.05);
      display: flex;
      flex-direction: column;
      justify-content: space-evenly;
      padding: 10px 25px;
    }
  }
}
@media screen and (max-width: 762px) {
  section {
    padding-top: 0 !important;
    padding-bottom: 25px !important;
    & .about {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 10px;
      & img {
        border-top: 4px solid $primary;
        border-bottom: none;
        max-width: 100%;
        max-height: 100%;
        border-top-left-radius: 25px;
        border-top-right-radius: 25px;
        border-bottom-left-radius: 0px;
        box-shadow: 0.5px 0px 5px 1px rgba(0,0,0,0.3);
      }
      & .about-info {
        padding-top: 20px !important;
        padding-bottom: 20px !important;
        border-top: 8px solid $primary;
        border-bottom: 4px solid $primary;
        border-bottom-right-radius: 25px;
        border-bottom-left-radius: 25px;
        border-top-right-radius: 0;
        box-shadow: 0.5px 0px 5px 1px rgba(0,0,0,0.05);
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        padding: 10px 25px;
      }
    }
  }
}
</style>