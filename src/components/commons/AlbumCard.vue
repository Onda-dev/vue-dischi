<template>
  <div class="album p-4 d-flex-col">
      <img src="https://www.emme2servizi.it/wp-content/uploads/2020/12/no-image.jpg" alt="">
      <h3 class="title">Titolo</h3>
      <div class="author">Autore</div>
      <div class="year">1999</div>
  </div>
</template>

<script>
export default {
    name: 'AlbumCard',
    props: {
        album: Object,
    }
}
</script>

<style lang="scss" scoped>
.album {
    text-align: center;
    background-color: #2E3A46;
}
img {
    width: 100%;
    margin-bottom: 1.25rem;
}
</style>