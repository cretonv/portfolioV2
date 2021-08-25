<template>
  <div class="project-highlight-line">
    <div v-for="project in projects" :key="project.title" class="project-item">
      <h3>{{ project.title }}</h3>
      <div>{{ project.project_type }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectsHighlight',
  props: {
    projects: {
      required: true
    }
  }
}
</script>

<style scoped>

</style>
