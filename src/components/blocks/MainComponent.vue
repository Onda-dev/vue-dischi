<template>
  <main class="p-5">
    <div class="container">
        <section-album/>    
    </div>
  </main>
</template>

<script>
import SectionAlbum from '../sections/SectionAlbum.vue'
export default {
  components: { SectionAlbum },
    name: 'MainComponent'
}
</script>

<style lang="scss" scoped>
main {
    background-color: #1E2D3B;
}
</style>