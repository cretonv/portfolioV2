<template>
  <div class="line-container">
    <div class="item">
      <img class="symbol" src="~/assets/img/symbolsLine/air.svg">
      <div class="label">
        {{ textArrray[0] }}
      </div>
    </div>
    <div class="item">
      <img class="symbol" src="~/assets/img/symbolsLine/water.svg">
      <div class="label">
        {{ textArrray[1] }}
      </div>
    </div>
    <div class="item">
      <img class="symbol" src="~/assets/img/symbolsLine/fire.svg">
      <div class="label">
        {{ textArrray[2] }}
      </div>
    </div>
    <div class="item">
      <img class="symbol" src="~/assets/img/symbolsLine/earth.svg">
      <div class="label">
        {{ textArrray[3] }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SymbolsLine',
  props: {
    textArrray: {
      type: Array,
      required: true,
      length: 4
    }
  }
}
</script>

<style lang="scss" scoped>
.line-container {
  display: flex;
  flex-flow: row nowrap;
  max-width: 715px;
  margin: 0 auto 32px;

  .item {
    width: 25%;
    display: flex;
    align-items: center;
    flex-flow: column wrap;
    .symbol {
      width: 106px;
      height: 85px;
    }
    .label {
      margin-top: 8px;
      font-family: Lato;
      font-size: 15px;
      font-weight: 600;
      color: #D9D9D9;
    }
  }
}
</style>
