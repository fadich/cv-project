<template>
  <div class="project-preview">
    <div v-if="preview.frame">
      <span class="pull-right">
          <a :href="preview.url" target="_blank">
              <span class="glyphicon glyphicon-share"></span>
          </a>
          <button class="btn btn-xs btn-link increase-preview">
              <span class="glyphicon glyphicon-resize-full"></span>
          </button>
      </span>
      <iframe class="frame" :src="preview.url" scrolling="no" v-if="showFrames"></iframe>
    </div>
    <a :href="preview.url" target="_blank">{{ preview.url }}</a>
  </div>
</template>

<script>
  export default {
    name: 'ProjectPreview',
    props: ['preview'],
    data () {
      return {
        showFrames: false
      }
    },
    mounted () {
      setTimeout(function () {
        this.showFrames = true
      }.bind(this), 1500)
    }
  }
</script>

<style lang="scss" scoped>
  .project-preview {
    margin: 0 0 10px 0;

    .frame {
      width: 100%;
      height: 40vh;
      overflow: hidden;
      border: 1px solid #CCCCCC;
      -moz-transform: scale(1.0);
      -moz-transform-origin: 0 0;
      -o-transform: scale(1.0);
      -o-transform-origin: 0 0;
      -webkit-transform: scale(1.0);
      -webkit-transform-origin: 0 0;
    }
    .increase-preview {
    }
  }
</style>
