<template>
  <div>
    <h2>Resume Page</h2>
    <vue-pdf-embed :source="resume" />

  </div>
</template>

<script>
import VuePdfEmbed from 'vue-pdf-embed/dist/vue2-pdf-embed'

export default {
  data (){
      return {
        resume: 'Charlene Mitchell JResume.pdf'
      }
  },

  components: {
    VuePdfEmbed
  }

}
</script>

<style>

</style>