<template>
  <div class="base-spinner fa-3x" v-if="visible">
    <i class="fas fa-circle-notch fa-spin"></i>
  </div>
</template>

<script>
export default {
  data () {
    return {
      visible: false
    }
  },
  created () {
    this.$root.$on('Spinner::show', this.toogleSpinner)
    this.$root.$on('Spinner::hide', this.toogleSpinner)
  },
  methods: {
    toogleSpinner () {
      this.visible = !this.visible
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/variables';

.base-spinner {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  z-index: 1000000;
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: $dark-medium;
  color: $featured;
}
</style>
