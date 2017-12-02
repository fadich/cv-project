<template>
  <div class="project-item">

    <div class="row">
      <div class="col-md-12">
        <h2>{{ project.name }}</h2>

        <project-preview v-for="(link, index) in project.links" v-bind:preview="link" :key="index"></project-preview>

      </div>
    </div>

    <div class="row">
      <div class="col-md-12">
        <p>{{ project.description }}</p>
      </div>
    </div>
    <hr>
  </div>
</template>

<script>
  import ProjectPreview from '@/components/ProjectPreview'

  export default {
    name: 'Project',
    props: ['project'],
    components: { ProjectPreview }
  }
</script>
