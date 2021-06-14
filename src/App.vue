<template>
  <div id="app">
    <base-spinner />
    <button @click="showSpinner">Show Spinner</button>
    <!-- <router-view/> -->
  </div>
</template>

<script>
import BaseSpinner from './components/global/BaseSpinner.vue'

export default {
  name: 'App',
  components: {
    BaseSpinner
  },
  methods: {
    showSpinner () {
      this.$root.$emit('Spinner::show')
    }
  },
  mounted () {
    console.log(this.$firebase)
  }
}
</script>

<style lang="scss">

</style>
