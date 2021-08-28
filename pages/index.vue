<template>
  <div class="full-content">
    <HomeLanding />
    <TitleH2 icon-name="sun" text-value="Mon travail" />
    <SymbolsLine :text-arrray="textArray"/>
    <ProjectsHighlight :projects="sortProjects" />
    <TitleH2 icon-name="salt" text-value="À propos de moi" />
    <Presentation />
  </div>
</template>

<script>
import HomeLanding from '@/components/HomeLanding'
import TitleH2 from '@/components/TitleH2'
import SymbolsLine from '@/components/SymbolsLine'
import ProjectsHighlight from '@/components/ProjectsHighlight'
import Presentation from '@/components/Presentation'
export default {
  head: {
    bodyAttrs: {
      class: 'no-margin'
    }
  },
  components: { TitleH2, HomeLanding, SymbolsLine, ProjectsHighlight, Presentation },
  data: () => {
    return {
      textArray: ['Conception', 'UX Design', 'Développement', 'Team Lead']
    }
  },
  async asyncData ({ $content }) {
    const projects = await $content('projects').fetch()
    const sortProjects = [projects[0], projects[1], projects[2]]
    return {
      projects,
      sortProjects
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
