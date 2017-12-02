<template>
  <div class="projects">
    <project v-for="(project, index) in projects" v-bind:project="project" :key="index"></project>
  </div>
</template>

<script>
import Project from '@/components/Project'

export default {
  name: 'Projects',
  data () {
    return {
      projects: projects  // window.projects
    }
  },
  components: {
    Project
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>

</style>
