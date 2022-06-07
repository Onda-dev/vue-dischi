<template>
  <div class="album-grid">
      <div class="row">
          <div class="col-3" >
              <AlbumCard v-for="(album, index) in albums" :key="index"/>
          </div>
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
            this.albums = response.data;
            console.log(response.data);
        })
        .catch((error) => {
            console.log(error);
        })
    }
}
</script>

<style lang="scss" scoped>

</style>