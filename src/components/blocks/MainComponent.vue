<template>
  <main class="p-4">
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
    display: flex;
    align-items: center;
    background-color: #1E2D3B;
    overflow: auto;
}
</style>