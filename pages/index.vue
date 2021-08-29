<template>
  <div class="full-content">
    <HomeLanding />
    <TitleH2 icon-name="sun" text-value="Mon travail" />
    <SymbolsLine :text-arrray="textArray"/>
    <ProjectsHighlight :projects="sortProjects" />
    <TitleH2 icon-name="salt" text-value="À propos de moi" />
    <Presentation />
    <div class="experience-bloc">
      <SchoolExperience :exp-array="schoolExp" />
    </div>
  </div>
</template>

<script>
import HomeLanding from '@/components/HomeLanding'
import TitleH2 from '@/components/TitleH2'
import SymbolsLine from '@/components/SymbolsLine'
import ProjectsHighlight from '@/components/ProjectsHighlight'
import Presentation from '@/components/Presentation'
import SchoolExperience from '@/components/SchoolExperience'
export default {
  head: {
    bodyAttrs: {
      class: 'no-margin'
    }
  },
  components: { TitleH2, HomeLanding, SymbolsLine, ProjectsHighlight, Presentation, SchoolExperience },
  data: () => {
    return {
      textArray: ['Conception', 'UX Design', 'Développement', 'Team Lead']
    }
  },
  async asyncData ({ $content }) {
    const projects = await $content('projects').fetch()
    const sortProjects = [projects[0], projects[1], projects[2]]
    const schoolExp = await $content('formations').fetch()
    return {
      projects,
      sortProjects,
      schoolExp
    }
  }
}
</script>

<style scoped lang="scss">
.full-content {
  background: #303030;
  padding-bottom: 100px;
}
.experience-bloc {
  max-width: 816px;
  margin: 24px auto;
  display: flex;
  flex-flow: row nowrap;
}
</style>
