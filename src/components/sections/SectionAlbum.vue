<template>
  <div class="album-grid">
      <div class="row">
        <AlbumCard class="col-2" v-for="(album, index) in albums" :key="index" :album="album"/>
      </div>
  </div>
</template>

<script>
import axios from 'axios';
import AlbumCard from '../commons/AlbumCard'

export default {
    name: 'SectionAlbum',
    data() {
        return {
            albums: [],
        };
    },
    components: {
        AlbumCard
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
    }
}
</script>

<style lang="scss" scoped>
.row {
    display: flex;
    justify-content: center;
    gap: 1.25rem;
}

</style>