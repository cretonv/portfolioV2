<template>
  <div class="full-content">
    <HomeLanding />
    <TitleH2 icon-name="sun" text-value="Mon travail" />
  </div>
</template>

<script>
import HomeLanding from '@/components/HomeLanding'
import TitleH2 from '@/components/TitleH2'
export default {
  head: {
    bodyAttrs: {
      class: 'no-margin'
    }
  },
  components: { TitleH2, HomeLanding }
}
</script>

<style scoped lang="scss">
.full-content {
  background: #303030;
}
</style>
