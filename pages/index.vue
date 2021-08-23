<template>
  <div class="full-content">
    <HomeLanding />
    <TitleH2 icon-name="sun" text-value="Mon travail" />
    <SymbolsLine :text-arrray="textArray"/>
  </div>
</template>

<script>
import HomeLanding from '@/components/HomeLanding'
import TitleH2 from '@/components/TitleH2'
import SymbolsLine from '@/components/SymbolsLine'
export default {
  head: {
    bodyAttrs: {
      class: 'no-margin'
    }
  },
  components: { TitleH2, HomeLanding, SymbolsLine },
  data: () => {
    return {
      textArray: ['Conception', 'UX Design', 'Développement', 'Team Lead']
    }
  }
}
</script>

<style scoped lang="scss">
.full-content {
  background: #303030;
  padding-bottom: 100px;
}
</style>
