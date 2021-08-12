<template>
  <a :href="linkTo" class="btn">
    <unicon :name="iconName" fill="#303030" height="29" width="29" />
    <span class="text">{{ textContent }}</span>
  </a>
</template>

<script>
export default {
  name: 'ButtonDefault',
  props: {
    iconName: {
      type: String,
      required: true
    },
    textContent: {
      type: String,
      required: true
    },
    linkTo: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped lang="scss">
.btn {
  background: #D9D9D9;
  color: #303030;
  border-radius: 8px;
  width: fit-content;
  padding: 2px;
  display: flex;
  align-items: center;
  text-decoration: none;
  .text {
    margin: 0 12px;
    font-family: Lato;
    font-size: 16px;
    font-weight: 600;
  }
}
</style>
