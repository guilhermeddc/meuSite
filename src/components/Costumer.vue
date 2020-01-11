<template>
  <section class="costumer">
    <div class="container costumer-body">
      <a :href="links.Poderosa" target="”_blank”" rel="”noopener”">
        <img :src="Poderosa" :alt="`A Podereosa ${alt}`" />
      </a>
      <a :href="links.AndersonFotos" target="”_blank”" rel="”noopener”">
        <img :src="AndersonFotos" :alt="`Anderson Fotos ${alt}`" />
      </a>
      <a :href="links.EspacoRelax" target="”_blank”" rel="”noopener”">
        <img :src="EspacoRelax" :alt="`Espaco Relax ${alt}`" />
      </a>
    </div>
  </section>
</template>

<script>
import Poderosa from "../assets/images/Poderosa.png";
import AndersonFotos from "../assets/images/Anderson_Fotos.png";
import EspacoRelax from "../assets/images/Espaco_Relax.png";

export default {
  name: "Costumer",
  data() {
    return {
      Poderosa,
      AndersonFotos,
      EspacoRelax,
      alt: " - Guilherme Rodrigues Web Designer, Desenvolvedor Web & Mobile",
      links: {
        Poderosa: 'https://www.apoderosasm.com.br/',
        AndersonFotos: 'https:///www.andersonfotos.com.br/',
        EspacoRelax: 'https:///www.espacorelax.com.br/',
      },
    };
  }
};
</script>

<style lang="scss" scoped>
.costumer {
  background-image: url("../assets/images/concert.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
  padding: 100px 0;
  & .costumer-body {
    display: flex;
    justify-content: space-around;
    align-items: center;
    & img {
      border-radius: 25px;
      padding: 5px;
      width: 220px;
      
    }
  }
}
</style>