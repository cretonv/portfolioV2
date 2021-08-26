<template>
  <div class="project-highlight-line">
    <div v-for="project in projects" :key="project.title" class="project-item">
      <div class="content">
        <h3>{{ project.title }}</h3>
        <div class="project-type">
          {{ project.project_type }}
        </div>
        <div class="project-techno">
          {{ project.techno_line }}
        </div>
        <ProjectSymbolColumn :conception="project.conception_label" :ux="project.ux_label" :development="project.development_label" :team-lead="project.team_lead_label" />
      </div>
      <img :src="require(`~/assets/uploads/${images[project.title]}`)">
    </div>
  </div>
</template>

<script>
import ProjectSymbolColumn from '@/components/ProjectSymbolColumn'
export default {
  name: 'ProjectsHighlight',
  components: { ProjectSymbolColumn },
  props: {
    projects: {
      type: Array,
      required: true
    }
  },
  computed: {
    images () {
      const allImagesUrl = []
      this.projects.forEach((project) => {
        const urlFiltered = project.thumbnail.match(/([^/]+)[/]?$/)
        allImagesUrl[project.title] = urlFiltered[0]
      })
      return allImagesUrl
    }
  }
}
</script>

<style lang="scss" scoped>
.project-highlight-line {
  display: flex;
  flex-flow: row nowrap;

  .project-item {
    width: 33.3%;
    height: 588px;
    position: relative;
    &::after {
      content: "";
      position: absolute;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      opacity: 0.37;
      background: #303030;
      z-index: 1;
    }
    img {
      object-fit: cover;
      object-position: center;
      width: 100%;
      height: 588px;
      position: absolute;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      z-index: 0;
    }
    .content {
      position: relative;
      z-index: 2;
      padding: 24px;
      height: 540px;
      h3 {
        margin: 0;
        font-family: Lato;
        font-weight: 600;
        font-size: 30px;
        text-transform: uppercase;
        color: #D9D9D9;
      }
      .project-type {
        font-family: Lato;
        font-weight: 500;
        font-size: 30px;
        text-transform: uppercase;
        color: #D9D9D9;
      }
      .project-techno {
        font-family: Lato;
        font-weight: 100;
        font-size: 20px;
        text-transform: uppercase;
        color: #D9D9D9;
        position: absolute;
        bottom: 24px;
        left: 24px;
        transform: rotate(-90deg) translateY(24px);;
        transform-origin: bottom left;
      }
    }
  }
}
</style>
