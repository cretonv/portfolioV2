<template>
  <div class="title-container">
    <img :src="require(`~/assets/img/titleSvg/${iconName}.svg`)" />
    <h2>{{ textValue }}</h2>
  </div>
</template>

<script>
export default {
  name: 'TitleH2',
  props: {
    textValue: {
      type: String,
      required: true
    },
    iconName: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped lang="scss">
  .title-container {
    position: relative;
    max-width: fit-content;
    margin: 24px auto 48px;

    h2 {
      font-family: Playfair;
      font-weight: 500;
      font-size: 70px;
      color: #D9D9D9;
      text-align: center;
      z-index: 1;
      position: relative;
      margin: 0;
    }
    img {
      position: absolute;
      width: 51px;
      height: auto;
      top: -5px;
      left: -23px;
      z-index: 0;
    }
  }
</style>
