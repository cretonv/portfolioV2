<template>
  <div class="school-experiences">
    <div v-for="expItem in expArray" :key="expItem.name" class="experience-item">
      <unicon class="icon" name="graduation-cap" fill="#303030" width="16" />
      <div class="date-line">
        {{ expItem.years }}
      </div>
      <div class="name">
        {{ expItem.name }}
      </div>
      <div class="description">
        {{ expItem.description }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SchoolExperience',
  props: {
    expArray: {
      type: Array,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.school-experiences {
  max-width: 399.5px;
  background: #D9D9D9;
  box-shadow: 0 46px 49px -2px rgba(0,0,0,0.15), 0 6px 6px -2px rgba(0,0,0,0.14), 0 2px 2px -2px rgba(0,0,0,0.13), 0 0 5px 0 rgba(171,171,171,0.50), inset 0 2px 1px 0 rgba(255,255,255,0.75);
  border-radius: 8px;
  display: flex;
  flex-flow: row wrap;
  padding-top: 16px;
  padding-bottom: 24px;
  .experience-item {
    width: 100%;
    position: relative;
    padding-left: 41px;
    padding-right: 16px;
    &::after {
      content: "";
      width: 1px;
      height: calc(100% - 16px);
      background: #303030;
      position: absolute;
      bottom: 0;
      left: 23px;
      transform: translateY(8px);
    }
    &:not(:last-of-type) {
      margin-bottom: 16px;
    }
    .icon {
      position: absolute;
      left: 16px;
      top: 0;
    }
    .date-line {
      font-family: Lato;
      font-weight: 300;
      font-size: 12px;
      color: #8B8B8B;
    }
    .name {
      font-family: Lato;
      font-weight: 600;
      font-size: 16px;
      color: #303030;
      margin-top: 8px;
      margin-bottom: 8px;
    }
    .description {
      font-family: Lato;
      font-weight: 400;
      font-size: 12px;
      color: #303030;
    }
  }
}
</style>
