<template>
<b-container>
  <b-row align-v="center" align-h="center">
    <b-col align-self="baseline" class="mt-5 rounded-lg border shadow-sm p-4 mb-4 mr-1 bg-white"><resumecont-test></resumecont-test></b-col>
    <b-col cols="8" align-self="stretch" class="mt-5 rounded-lg border shadow-sm p-4 mb-4 ml-1 bg-white"><resumetemp-default></resumetemp-default></b-col>
  </b-row>
</b-container>
</template>

<script>
import ResumeTemp_DefaultVue from '../components/ResumeTemp_Default.vue'
import ResumeCont_TestVue from '../components/ResumeCont_Test.vue'
// @ is an alias to /src


export default {
  name: 'Resume_Builder',
  components: {
    'resumetemp-default': ResumeTemp_DefaultVue,
    'resumecont-test': ResumeCont_TestVue
  }
}
</script>

<style scoped>

</style>
