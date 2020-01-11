<template>
  <section id="portfolio">
    <div class="container">
      <h2>Meu Portfólio</h2>
      <p>Conheça meus últimos clientes</p>
      <div class="portfolio-content">
        <CardPortfolio
          :image="Poderosa"
          name="A Poderosa"
          description="Comércio de Moda Plus Size"
        />
        <CardPortfolio
          :image="AndersonFotos"
          name="Anderson Fotos"
          description="Fotografia"
        />
        <CardPortfolio
          :image="EspacoRelax"
          name="Espaço Relax"
          description="Massoterapia"
        />
      </div>
    </div>
  </section>
</template>

<script>
import CardPortfolio from './CardPortfolio'
import Poderosa from '../assets/images/site_poderosa.jpg'
import AndersonFotos from '../assets/images/site_anderson_fotos.jpg'
import EspacoRelax from '../assets/images/site_espaco_relax.jpg'

export default {
  name: 'Portfolio',
  components: {
    CardPortfolio,
  },
  data() {
    return {
      Poderosa,
      AndersonFotos,
      EspacoRelax,
    }
  },
}
</script>

<style lang="scss" scoped>
#portfolio {
  background: $tertiary;
  padding-top: 50px;
  padding-bottom: 100px;
  & h2 {
    text-align: center;
    color: $light;
    padding: 50px 0 20px;
    font-size: 2em;
    text-shadow: 0px 1px 3px $dark;
  }
  & p {
    font-style: italic;
    color: $light;
    font-weight: 300;
    text-align: center;
    padding: 0 0 50px;
  }
  & .portfolio-content {
    display: flex;
    flex-wrap: wrap;
  }
}
</style>
