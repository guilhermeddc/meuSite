<template>
  <div class="button-fixed">
    <a :href="link" target="_blank" rel="”noopener”"><img :src="image" :alt="`${image} ${alt}`"></a>
  </div>
</template>

<script>
export default {
  name: 'ButtonFixed',
  props: {
    link: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      required: true,
    },
    alt: {
      type: String,
      required: true,
    },
  }
}
</script>

<style lang="scss" scoped>
.button-fixed {
  position: fixed;
  bottom: 30px;
  right: 30px;
  & a img {
    padding: 7px;
    width: 62px;
    background: #51EE6D;
    border-left: 2px solid $light;
    border-radius: 50%;
    box-shadow: 0 0 5px 2px rgba($color: $dark, $alpha: 0.12);
    transition: all 0.9s;
    &:hover {
      background: $primary;
      box-shadow: 0 0 5px 3px rgba($color: $dark, $alpha: 0.12);
    }
  }
}
@media screen and (max-width: 762px) {
  .button-fixed {
    bottom: 30px;
    right: 15px;
    & a img {
      width: 50px;
    }
  }
}
</style>
