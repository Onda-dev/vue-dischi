<template>
  <div class="album p-4 d-flex-col">
      <img :src="album.poster" alt="">
      <h3 class="title">{{album.title}}</h3>
      <div class="author">{{album.author}}</div>
      <div class="year">{{album.year}}</div>
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