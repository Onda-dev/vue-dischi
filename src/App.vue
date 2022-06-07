<template>
  <div id="app">
    <header-component/>
  </div>
</template>

<script>
import HeaderComponent from './components/blocks/HeaderComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent

  }
}
</script>

<style lang="scss">
@import 'assets/style/global.scss';
</style>
