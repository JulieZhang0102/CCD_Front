<template>
  <div id="app">
    <div id="nav">
      <top-header></top-header>
    </div>
    <router-view/>
  </div>
</template>

<script>
import TopHeaderVue from './components/TopHeader.vue'

export default {
  components: {
    'top-header': TopHeaderVue
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 55px;
}
</style>
