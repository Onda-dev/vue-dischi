<template>
  <div id="app">
    <header-component/>
    <main-component/>
  </div>
</template>

<script>
import HeaderComponent from './components/blocks/HeaderComponent.vue'
import MainComponent from './components/blocks/MainComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent
  }
}
</script>

<style lang="scss">
@import 'assets/style/global.scss';
</style>
