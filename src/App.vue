<template>
  <div id="app">
    <DetailsForm msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import DetailsForm from './components/DetailsForm.vue'

export default {
  name: 'app',
  components: {
    DetailsForm
  }
}
</script>

<style>
#app {
}
</style>
