<template>
  <div class="symbols-column">
    <img v-if="conception" class="symbol" src="~/assets/img/symbolsLine/air.svg">
    <img v-if="ux" class="symbol" src="~/assets/img/symbolsLine/water.svg">
    <img v-if="development" class="symbol" src="~/assets/img/symbolsLine/fire.svg">
    <img v-if="teamLead" class="symbol" src="~/assets/img/symbolsLine/earth.svg">
  </div>
</template>

<script>
export default {
  name: 'ProjectSymbolColumn',
  props: {
    conception: {
      type: Boolean,
      required: true
    },
    ux: {
      type: Boolean,
      required: true
    },
    development: {
      type: Boolean,
      required: true
    },
    teamLead: {
      type: Boolean,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.symbols-column {
  position: absolute;
  bottom: 16px;
  right: 8px;
  width: 47px;
  height: auto;
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  .symbol {
    height: 30px;
    width: auto;
    &:not(:last-of-type) {
      margin-bottom: 8px;
    }
  }
}
</style>
