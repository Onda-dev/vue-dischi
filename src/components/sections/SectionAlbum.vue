<template>
  <div class="album-grid">
      <select-genre @filter="filterGenre"/>
      <div class="row pt-4">
        <AlbumCard class="col-2" v-for="(album, index) in albumsFiltered" :key="index" :album="album"/>
      </div>
  </div>
</template>

<script>
import axios from 'axios';
import AlbumCard from '../commons/AlbumCard'
import SelectGenre from '../commons/SelectGenre.vue';

export default {
    name: 'SectionAlbum',
    data() {
        return {
            albums: [],
            albumsFiltered: []  
        };
    },
    components: {
        AlbumCard,
        SelectGenre
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.albums = response.data.response
            console.log(response.data.response);
        })
        .catch((error) => {
            console.log(error);
        })
    },
    methods: {
        filterGenre(searchInput) {
            this.albumsFiltered = this.albums.filter((elm) => elm.genre.toLowerCase().includes(searchInput.toLowerCase()))
            console.log(this.albumsFiltered)
        }
    }
}
</script>

<style lang="scss" scoped>
.album-grid {
    text-align: center;
}
.row {
    display: flex;
    justify-content: center;
    gap: 1.25rem;
}

</style>