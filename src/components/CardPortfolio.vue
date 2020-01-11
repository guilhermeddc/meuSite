<template>
  <div class="card-portfolio">
    <img :src="image" alt="Image of site">
    <div class="card-footer">
      <h3>{{ name }}</h3>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardPortfolio',
  props: {
    image: {
      type: String,
    },
    name: {
      type: String,
      default: 'Name of site'
    },
    description: {
      type: String,
      default: 'Description of site'
    },
  },
}
</script>

<style lang="scss" scoped>
.card-portfolio {
  flex: 1;
  margin: 10px;
  background: $light;
  border-radius: 5px;
  padding: 10px;
  box-shadow: 0 0 2px 1px rgba($color: $dark, $alpha: 0.5);
  transition: all 0.3s;
  &:hover {
    opacity: 0.8;
    box-shadow: 0 0 5px 2px rgba($color: $dark, $alpha: 0.5);
    background: $secondary;
    color: $light;
  }
  & img {
    border-radius: 5px;
    box-shadow: 0 0 2px 1px rgba($color: $dark, $alpha: 0.5);
    margin-top: -25px;
  }
  & .card-footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 20px;
    & h3 {
      font-size: 1.8em;
      text-shadow: 0px 1px 3px $dark;
      padding: 0 0 10px;
    }
    & p {
      font-size: 1em;
      text-shadow: 0px 1px 1px $dark;
      font-style: italic;
      padding: 0 0 10px;
    }
  }
}
</style>
